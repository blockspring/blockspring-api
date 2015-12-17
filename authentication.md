# Authentication

## Register an application

You can register an application at: [https://auth.blockspring.com/oauth/applications](https://auth.blockspring.com/oauth/applications)

After registering your application, you will receive a Client ID and Client Secret to be used to acquire an access token on behalf of a user.

In order to register your application, you will have to specify one or more callback URLs for use in the oAuth handshake. The domains of these urls will be used to validate any requests via our Javascript SDK.

`Note: All callback urls must be served over https.`

## Getting access tokens

There are two ways to get an access token:

1. For most apps, you'll want to use the [Authorization Code Flow](#authorization-code-flow)
2. For client side javascript apps that don't have a server/backend, you can use the [Implicit Grant Flow](#implicit-grant-flow).

> Ruby applications can use our [omniauth provider](https://github.com/blockspring/omniauth-blockspring) to quickly get up and running.

### Authorization Code Flow

1. Redirect the user's browser to the authentication URL:

  ```
  https://auth.blockspring.com/oauth/authorize
    ?response_type=code
    &client_id=[your client id]
    &redirect_uri=[a redirect URI]
  ```

2. If the user authorizes your application, they will be redirected to your callback url:

  ```
  https://[your redirect URI]/?code=[code]
  ```

3. On your server you should exchange this code for an access_token

  ```
  POST https://auth.blockspring.com/oauth/token
  ```

  Post Body:

  ```
  client_id=[your client id]
  &client_secret=[your client secret]
  &grant_type=authorization_code
  &redirect_uri=[same redirect URI from authorize request]
  &code=[code received]
  ```

4. We will respond with an access token

  ```javascript
  {
    "token_type" : "bearer",
    "created_at" : 1435644007,
    "scope" : "library run",
    "access_token" : "at_00426fc5cb3b49092a65cdeee030f4ed389fccb142010d46cb157306b4ee5384"
  }
  ```

5. You can now make [Authenticated Requests](#authenticated-requests)!


### Implicit Grant Flow

1. Redirect the user's browser to the authentication URL:

  ```
  https://auth.blockspring.com/oauth/authorize
    ?response_type=token
    &client_id=[your client id]
    &redirect_uri=[a redirect URI]
  ```

2. If the user authorizes your application, they will be redirected to your callback url:

  ```
  https://[your redirect URI]/#access_token=[code]&token_type=bearer
  ```

3. You can now make [Authenticated Requests](#authenticated-requests)!



## Scopes

Blockspring currently only as two scopes. These scopes are enabled by default and do not need to be specified.

- `library`: Make authenticated requests to the http API
- `run`: Run blocks on behalf of the user via run.blockspring.com

## Authenticated Requests

All requests to the Blockspring API require authentication. You can authenticate a request by passing a user's access token.

- Query string parameter

  ```
  curl https://api.blockspring.com/v0/me?access_token=[access_token]
  ```

- Authorization header

  ```
  curl -H "Authorization: Bearer [access_token]" https://api.blockspring.com/v0/me
  ```
