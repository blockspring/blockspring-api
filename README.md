# Blockspring API Documentation (Closed Beta - v0)

This repository contains the documentation for the Blockspring API.

## Authentication

Blockspring uses oAuth2 for authenticating applications.

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
https://api.blockspring.com/v0/marco?callback=myfunction
```

### Response

```
myfunction({"shout":"POLO!"});
```

### CORS

\# TODO

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

## Executing Blocks

\# TODO

## Javascript SDK

\# TODO

## Changelog

You can view the changelog in [CHANGELOG.md](/CHANGELOG.md)


## Terms of Service

Please review our [Terms of Service](https://www.blockspring.com/about/tos).
