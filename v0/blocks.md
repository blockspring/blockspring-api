# Blocks

1. [Get a Block](#get-a-block)


## Get a Block

Get meta data about a block.

### Endpoint

`GET /v0/blocks/:block_id`

### Parameters

None

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

```javascript
{
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
    "id": "invite-blockspring-slack",
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
}
```
