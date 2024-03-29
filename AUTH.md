# Authenticating to Permanent with FusionAuth

Permanent uses [FusionAuth](https://fusionauth.io/) as our
[IdP](https://en.wikipedia.org/wiki/Identity_provider).

## Getting an access token

### FusionAuth client

To get access tokens, your client will need to be created in
Permanent's FusionAuth account.  Someone at Permanent will set that up
for you and give you a `CLIENT_ID` and `CLIENT_SECRET`.  The
`AUTH_HOST` will also need to be set.  We use one host
(auth.permanent.org) for prod and another
(permanent-dev.fusionauth.io) for all other environments.

### Logging in via FusionAuth

OAuth with FusionAuth is covered in their documentation
[here](https://fusionauth.io/docs/v1/tech/oauth/endpoints/).
Essentially, we follow a two step approach:

1. Direct the user to FusionAuth to log in.  They'll be redirected
back to your application (using a link that is set in the FusionAuth
client) and the response will contain an authorization code.

2. Exchange the Authorization Code for a Token

Mobile apps should use PKCE.  See [this
article](https://www.oauth.com/oauth2-servers/oauth-native-apps/) for
an overview of special considerations for native applications.

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

### Refreshing the token

The original token you receive from FusionAuth will expire.  It will
have a refresh token if you request the token with the
`offline_access` scope and the FusionAuth client has refresh enabled.
When the token expires, use this refresh token to get a new access
token and send that to Permanent in the Authorization header.  We
recommend using refresh tokens for flows that will be taking place
without user input - e.g., a long running script.  If the user will be
present throughout, then don't use a refresh token.  Instead, bounce
back through the FusionAuth login flow.  For a mobile app, for
example, the user won't see this happening since the mobile browser
will retain the login credentials.  When necessary, though, the user
will be prompted to log in again.

## Examples

For clients that use the
[node-sdk](https://github.com/PermanentOrg/node-sdk/), take a look at
how we authenticate from our [Etherpad
plugin](https://github.com/PermanentOrg/ep_permanent_exporter).

_Note: currently the node-sdk and Etherpad authentication flows are
still in `oauth` branches on those repositories.  We expect to have
those merged soon and will update this documentation accordingly._

## Creating a new user

Most new users will likely sign up through the web app
(permanent.org).  If your client allows sign up, though, you'll want
to use the existing sign up API and then, after the user has been
created, immediately prompt them to log in using the log in flow
above.  Once you have an access token you can proceed as normal.