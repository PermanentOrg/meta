# Authenticating to Permanent with FusionAuth

Permanent uses [FusionAuth](https://fusionauth.io/) as our
[IdP](https://en.wikipedia.org/wiki/Identity_provider).

## Getting an access token

### FusionAuth client

To get access tokens, your client will need to be created in
Permanent's FusionAuth account.  Someone at Permanent will set that up
for you and give you a `CLIENT_ID` and `CLIENT_SECRET`.

### Logging in via FusionAuth


## Sending the token in the request

This is described in [the back-end
repo](https://github.com/PermanentOrg/back-end/blob/main/docs/auth.md),
but since that is not yet open source, we reproduce it here.

The API can authenticate the user by accepting a JWT in the HTTP
Authorization header.

For example, calling the API endpoint to check if you are logged in might look like:

```
$ curl -v --header "Authorization: Bearer ${TOKEN}" \
  https://example.permanent.org/api/auth/loggedIn
```

To get one of these tokens for testing, the easiest way is to use the
[Resource Owner Password Credentials
Grant](https://datatracker.ietf.org/doc/html/rfc6749#section-4.3) flow
to generate a token. Make sure that the client you are using is
configured in the IdP to allow password grant authentication, and then
call:

```
$ curl -v \
  --request POST \
  --url 'https://auth-example.permanent.org/oauth2/token' \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type=password' \
  --data-urlencode "username=${EMAIL}" \
  --data-urlencode "password=${PASSWORD}" \
  --data "client_id=${CLIENT_ID}" \
  --data "client_secret=${CLIENT_SECRET}"
```

### Refreshing the token

The original token you receive from FusionAuth will expire.  It will
have a refresh token as long as you request the token with the
`offline_access` scope.  When the token expires, use this refresh
token to get a new access token and send that to Permanent in the
Authorization header.

## Creating a new user