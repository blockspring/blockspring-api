# Favorites

1. [List Favorites](#list-favorites)


## List Favorites

Get a list of the current user's favorite blocks.

### Endpoint

`GET /v0/favorites`

### Parameters

| Name | Type | Description|
| --- | --- | --- |
| N/A | N/A | N/A |

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

```javascript
[
  {
    "id": "invite-blockspring-slack",
    "action_types": [
      {
        "created_at": "2015-09-17T00:31:28.368Z",
        "description": "Create, update, or delete data elsewhere.",
        "id": 4,
        "name": "Post Data",
        "updated_at": "2015-09-17T00:31:28.368Z"
      }
    ],
    "can_be_imported_to_organization": true,
    "can_be_unfavorited": true,
    "created_at": 1438731640,
    "description": "Blockspring has a wonderful Slack community for power users. Want in? Enter your email!",
    "favorite_url": "https://api.blockspring.com/v0/favorites/invite-blockspring-slack?access_token={access_token}",
    "formatted_tag_line": "Blockspring has a wonderful Slack community for power users. ...",
    "html_description": "<p>Blockspring has a wonderful Slack community for power users. Want in? Enter your email!</p>\n",
    "is_favorited": true,
    "is_imported_to_organization": false,
    "is_open_source": false,
    "is_public": true,
    "oauth": [],
    "organization_id": null,
    "parameters": [
      {
        "default": "paul@blockspring.com",
        "label": "User's email address",
        "name": "email",
        "type": "text"
      }
    ],
    "response_schema": {
      "$schema": "http://json-schema.org/draft-04/schema#",
      "properties": {
        "_blockspring_spec": {
          "type": "boolean"
        },
        "_errors": {
          "items": {
            "properties": {
              "message": {
                "type": "string"
              },
              "title": {
                "type": "string"
              }
            },
            "type": "object"
          },
          "type": "array"
        }
      },
      "title": "invite-yourself-to-blocksprings-slack-community",
      "type": "object"
    },
    "secrets": [],
    "tag": {
      "description": "Blockspring is indexing the world's APIs to make them easy to use for everyone!",
      "full_image_url": "https://static.blockspring.com/tag-icons/blockspring.png",
      "id": 363,
      "image_url": "blockspring.png",
      "name": "blockspring",
      "oauth": [],
      "readable_name": "Blockspring",
      "secrets": [],
      "url": "https://api.blockspring.com/v0/tags/363?access_token={access_token}"
    },
    "title": "Invite Yourself to Blockspring's Slack Community",
    "updated_at": 1438731684,
    "url": "https://api.blockspring.com/v0/blocks/invite-blockspring-slack?access_token={access_token}",
    "username": "bs",
    "uuid": "b03313b831a55ce7380cae5e64e2df69"
  },
  {
    "id": "bing-web-search",
    "action_types": [
      {
        "created_at": "2015-09-16T23:22:57.906Z",
        "description": "Block returns a single key whose value is an array of arrays or array of objects.",
        "id": 1,
        "name": "Get Tabular Data",
        "updated_at": "2015-09-16T23:22:57.906Z"
      }
    ],
    "can_be_imported_to_organization": true,
    "can_be_unfavorited": true,
    "created_at": 1431382419,
    "description": "Use the Bing web search API! Input a query, and get the top Bing search results.",
    "favorite_url": "https://api.blockspring.com/v0/favorites/bing-web-search?access_token={access_token}",
    "formatted_tag_line": "Use the Bing web search API! Input a query, and get the top B...",
    "html_description": "<p>Use the Bing web search API! Input a query, and get the top Bing search results.</p>\n",
    "is_favorited": true,
    "is_imported_to_organization": false,
    "is_open_source": true,
    "is_public": true,
    "oauth": [],
    "organization_id": null,
    "parameters": [
      {
        "default": "XBox 360",
        "help_text": "",
        "label": "Search Query",
        "name": "search_query",
        "optional": false,
        "placeholder": "XBox 360",
        "type": "text"
      },
      {
        "default": "0",
        "help_text": "The page number of search results to retrieve. This gets to a maximum of 20.",
        "label": "Page",
        "name": "page",
        "optional": true,
        "placeholder": "0",
        "type": "number"
      }
    ],
    "response_schema": {
      "$schema": "http://json-schema.org/draft-04/schema#",
      "properties": {
        "_blockspring_spec": {
          "type": "boolean"
        },
        "_errors": {
          "items": {},
          "type": "array"
        },
        "results": {
          "items": {
            "properties": {
              "Description": {
                "type": "string"
              },
              "DisplayUrl": {
                "type": "string"
              },
              "ID": {
                "type": "string"
              },
              "Title": {
                "type": "string"
              },
              "Url": {
                "type": "string"
              },
              "__metadata": {
                "properties": {
                  "type": {
                    "type": "string"
                  },
                  "uri": {
                    "type": "string"
                  }
                },
                "type": "object"
              }
            },
            "required": [
              "Description",
              "Title",
              "Url",
              "__metadata",
              "DisplayUrl",
              "ID"
            ],
            "type": "object"
          },
          "type": "array"
        }
      },
      "title": "bing-web-search",
      "type": "object"
    },
    "secrets": [
      {
        "description": "1. Visit here: https://datamarket.azure.com/dataset/bing/search\r\n2. Click one of the \"Sign up\" buttons (eg free account is ~ 5k requests per month)\r\n3. Agree to all the terms.\r\n4. Go to your account: https://datamarket.azure.com/account\r\n5. Copy your \"primary account key\" into Blockspring.",
        "html_description": "<ol>\n<li>Visit here: <a rel=\"nofollow\" href=\"https://datamarket.azure.com/dataset/bing/search\" target=\"_blank\">https://datamarket.azure.com/dataset/bing/search</a></li>\n<li>Click one of the &quot;Sign up&quot; buttons (eg free account is ~ 5k requests per month)</li>\n<li>Agree to all the terms.</li>\n<li>Go to your account: <a rel=\"nofollow\" href=\"https://datamarket.azure.com/account\" target=\"_blank\">https://datamarket.azure.com/account</a></li>\n<li>Copy your &quot;primary account key&quot; into Blockspring.</li>\n</ol>\n",
        "id": 33,
        "name": "Bing Search API Key",
        "set_value_url": "https://auth.blockspring.com/secrets/33/set?api_key={access_token}&block_id=bing-web-search",
        "value_is_set": true,
        "variable_name": "bing_key"
      }
    ],
    "tag": {
      "description": "Search the web, images, videos, and news.",
      "full_image_url": "https://static.blockspring.com/tag-icons/bing.jpg",
      "id": 117,
      "image_url": "bing.jpg",
      "name": "bing-search",
      "oauth": [],
      "readable_name": "Bing Search",
      "secrets": [
        {
          "description": "1. Visit here: https://datamarket.azure.com/dataset/bing/search\r\n2. Click one of the \"Sign up\" buttons (eg free account is ~ 5k requests per month)\r\n3. Agree to all the terms.\r\n4. Go to your account: https://datamarket.azure.com/account\r\n5. Copy your \"primary account key\" into Blockspring.",
          "html_description": "<ol>\n<li>Visit here: <a rel=\"nofollow\" href=\"https://datamarket.azure.com/dataset/bing/search\" target=\"_blank\">https://datamarket.azure.com/dataset/bing/search</a></li>\n<li>Click one of the &quot;Sign up&quot; buttons (eg free account is ~ 5k requests per month)</li>\n<li>Agree to all the terms.</li>\n<li>Go to your account: <a rel=\"nofollow\" href=\"https://datamarket.azure.com/account\" target=\"_blank\">https://datamarket.azure.com/account</a></li>\n<li>Copy your &quot;primary account key&quot; into Blockspring.</li>\n</ol>\n",
          "id": 33,
          "name": "Bing Search API Key",
          "set_value_url": "https://open.blockspring.com/secrets/33/set?api_key={access_token}&block_id=bing-web-search",
          "value_is_set": true,
          "variable_name": "bing_key"
        }
      ],
      "url": "https://api.blockspring.com/v0/tags/117?access_token={access_token}"
    },
    "title": "Web Search",
    "updated_at": 1443416052,
    "url": "https://api.blockspring.com/v0/blocks/bing-web-search?access_token={access_token}",
    "username": "bs",
    "uuid": "9157be8d6e9ac8f19b3cb1014f7795ef"
  }
]
```
