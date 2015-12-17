# Blockspring API Documentation (Closed Beta - v0)

This repository contains the documentation for the Blockspring API.

## Authentication

Blockspring uses oAuth2 for authenticating applications.

[View the Authentication Documentation](https://github.com/blockspring/blockspring-api/blob/master/authentication.md)

Manage your apps: [Developer App Dashboard](https://auth.blockspring.com/oauth/applications)

## Javascript SDK

\# TODO

## HTTP API

### Basics

__API Base URL:__ `https://api.blockspring.com/v0/`  
__Response format:__ json

### JSONP

\# TODO

### CORS

\# TODO

### Endpoints

#### Test

Endpoints for testing API clients and access tokens.

| Endpoint | Description |
|-|
| `GET` [/v0/marco](https://github.com/blockspring/blockspring-api/blob/master/v0/test.md#marco) | Test simple `GET` request. Replies `200` "POLO!" |
| `POST` [/v0/echo](https://github.com/blockspring/blockspring-api/blob/master/v0/test.md#echo) | Test simple `POST` request. Replies `200` with payload you send. |

## Changelog

You can view the changelog in [CHANGELOG.md](https://github.com/blockspring/blockspring-api/blob/master/CHANGELOG.md)


## Terms of Service

Please review our [Terms of Service](https://www.blockspring.com/about/tos).
