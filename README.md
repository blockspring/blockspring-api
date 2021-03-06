# Blockspring API Documentation (Beta - v0)

This repository contains the documentation for the Blockspring API.

- [Authentication](#authentication)
- [HTTP API](#http-api)
  - [Basics](#basics)
  - [JSONP](#jsonp)
  - [CORS](#cors)
- [Endpoints](#endpoints)
  - [Test](#test)
  - [User](#user)
  - [Favorites](#favorites)
  - [Tags](#tags)
  - [Organizations](#organizations)
- [Executing Blocks](#executing-blocks)
- [Javascript SDK](#javascript-sdk)

## Authentication

Blockspring uses OAuth2 for authenticating applications.

[View the Authentication Documentation](https://github.com/blockspring/blockspring-api/blob/master/authentication.md#authentication)

Manage your apps: [Developer App Dashboard](https://auth.blockspring.com/oauth/applications)

## HTTP API

### Basics

- __API Base URL:__ `https://api.blockspring.com/v0/`
- __Response format:__ json
- __Request Authentication:__ [Making Authenticated Requests](/authentication.md#authenticated-requests)

### JSONP

The Blockspring v0 API supports [JSONP](https://en.wikipedia.org/wiki/JSONP) for `GET` requests. Add a `callback` query string parameter to requests:

#### Request

```
https://api.blockspring.com/v0/me?callback=myfunction
```

#### Response

```javascript
/**/myfunction({
  "meta": {
    "status": 200,
    "X-Blockspring-API-Version": "v0"
  },
  "data": {,
    "id": 3,
    "username": "jtokoph",
    "name": "Jason Tokoph",
    "favorites_url": "https://api.blockspring.com/v0/favorites?access_token={access_token}",
    "url": "https://api.blockspring.com/v0/me?access_token={access_token}",
    "organization": {
      "subdomain": "blockspring",
      "name": "Blockspring",
      "url": "https://api.blockspring.com/v0/organization?access_token={access_token}"
    }
  }
})
```

### CORS

The Blockspring API supports Cross Origin Resource Sharing (CORS) for AJAX requests from any origin.

## Endpoints

### [Test](https://github.com/blockspring/blockspring-api/blob/master/v0/test.md#test)

Endpoints for testing API clients and access tokens.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/marco](/v0/test.md#test-get) | Test simple `GET` request. Replies `200` "POLO!" |
| `POST` | [/v0/echo](/v0/test.md#test-post) | Test simple `POST` request. Replies `200` with payload you send. |

### [User](/v0/user.md#user)

Endpoints for getting User information.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/me](/v0/user.md#get-user-info) | Get user information for access token |

### [Favorites](/v0/favorites.md#favorites)

Endpoints for getting a user's favorite blocks.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/favorites](/v0/favorites.md#list-favorites) | Get user's favorite blocks |

### [Tags](/v0/tags.md#tags)

Endpoints for getting tags on Blockspring.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/tags](/v0/tags.md#list-tags) | Get official Blockspring tags |
| `GET` | [/v0/tags/:tag_id](/v0/tags.md#get-a-tag) | Get tag and blocks with that tag |

### [Blocks](/v0/blocks.md#blocks)

Endpoints for getting block info.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/blocks/:block_id](/v0/blocks.md#get-a-block) | Get block metadata |

### [Organizations](/v0/organizations.md#organizations)

Endpoints for getting tags on Blockspring.

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | [/v0/organizations](/v0/organizations.md#get-organization-info) | Get information about the current user's organization |
| `GET` | [/v0/organizations/tags](/v0/organizations.md#get-a-tag) | Get an organization's tags |

## Executing Blocks

Blocks are executed via another system at `https://run.blockspring.com` instead of `https://api.blockspring.com`.

Authentication for running blocks is done with the same access_token retrieved via OAuth.

[View the Block Execution documentation](/block_execution.md#block-execution)

## Javascript SDK

The Blockspring Javascript SDK allows your website to interact with the Blockspring platform with a simple to use interface. It currently only supports opening a block form window for users to test and preconfigure block runs. More information can be found on the [Javascript SDK page](/javascript_sdk.md#javascript-sdk)

## Changelog

You can view the changelog in [CHANGELOG.md](/CHANGELOG.md)


## Terms of Service

Please review our [Terms of Service](https://www.blockspring.com/about/tos).
