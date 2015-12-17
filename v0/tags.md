# Tags

1. [List Tags](#list-tags)
2. [Get a Tag](#get-a-tag)

## List Tags

Get a list of the official tags on Blockspring.

### Endpoint

`GET /v0/tags`

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
    "description": "Natural Language Processing, Information Retrieval and Machine Learning tools for extracting meaning and insight from textual and visual content with ease.",
    "full_image_url": "https://static.blockspring.com/tag-icons/aylien.png",
    "id": 303,
    "image_url": "aylien.png",
    "name": "aylien",
    "oauth": [],
    "readable_name": "Aylien",
    "secrets": [
      {
        "description": "1) Visit https://developer.aylien.com/admin/applications/.\r\n2) Sign up (or sign in). If you signed up, make sure you verify your account in your email.\r\n3) From https://developer.aylien.com/admin/applications/, click on an app.\r\n4) Copy your Application Key into Blockspring.",
        "html_description": "<p>1) Visit <a rel=\"nofollow\" href=\"https://developer.aylien.com/admin/applications/\" target=\"_blank\">https://developer.aylien.com/admin/applications/</a>.<br>\n2) Sign up (or sign in). If you signed up, make sure you verify your account in your email.<br>\n3) From <a rel=\"nofollow\" href=\"https://developer.aylien.com/admin/applications/\" target=\"_blank\">https://developer.aylien.com/admin/applications/</a>, click on an app.<br>\n4) Copy your Application Key into Blockspring.</p>\n",
        "id": 92,
        "name": "Aylien Application Key",
        "set_value_url": "https://open.blockspring.com/secrets/92/set?api_key={access_token}&block_id=sentiment-analysis-with-aylien",
        "value_is_set": true,
        "variable_name": "aylien_application_key"
      },
      {
        "description": "1) Visit https://developer.aylien.com/admin/applications/.\r\n2) Sign up (or sign in). If you signed up, make sure you verify your account in your email.\r\n3) From https://developer.aylien.com/admin/applications/, click on an app.\r\n4) Copy your Application ID into Blockspring.",
        "html_description": "<p>1) Visit <a rel=\"nofollow\" href=\"https://developer.aylien.com/admin/applications/\" target=\"_blank\">https://developer.aylien.com/admin/applications/</a>.<br>\n2) Sign up (or sign in). If you signed up, make sure you verify your account in your email.<br>\n3) From <a rel=\"nofollow\" href=\"https://developer.aylien.com/admin/applications/\" target=\"_blank\">https://developer.aylien.com/admin/applications/</a>, click on an app.<br>\n4) Copy your Application ID into Blockspring.</p>\n",
        "id": 93,
        "name": "Aylien Application ID",
        "set_value_url": "https://open.blockspring.com/secrets/93/set?api_key={access_token}&block_id=sentiment-analysis-with-aylien",
        "value_is_set": true,
        "variable_name": "aylien_application_id"
      }
    ],
    "url": "https://api.blockspring.com/v0/tags/303?access_token={access_token}"
  },
  {
    "description": "Buffer is a software application designed to manage social networks, by providing the means for a user to schedule posts to Twitter, Facebook, and Linkedin.",
    "full_image_url": "https://static.blockspring.com/tag-icons/buffer.png",
    "id": 382,
    "image_url": "buffer.png",
    "name": "buffer",
    "oauth": [
      {
        "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=get-user-info-buffer",
        "id": 141,
        "provider": {
          "id": 18,
          "name": "Buffer",
          "omniauth_class": "bsbuffer",
          "slug": "buffer"
        },
        "value_is_set": false
      }
    ],
    "readable_name": "Buffer",
    "secrets": [],
    "url": "https://api.blockspring.com/v0/tags/382?access_token={access_token}"
  }
]
```

## Get a Tag

Get info and list of blocks for a tag.

### Endpoint

`GET /v0/tags/:tag_id`

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
{
  "blocks": [
    {
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
      "created_at": 1439251368,
      "description": "Returns social media profiles connected to a user's account.",
      "favorite_url": "https://api.blockspring.com/v0/favorites/profiles-information-buffer?access_token={access_token}",
      "formatted_tag_line": "Returns social media profiles connected to a user's account.",
      "html_description": "<p>Returns social media profiles connected to a user&#39;s account.</p>\n",
      "id": "profiles-information-buffer",
      "is_favorited": false,
      "is_imported_to_organization": false,
      "is_open_source": true,
      "is_public": true,
      "oauth": [
        {
          "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=profiles-information-buffer",
          "id": 141,
          "provider": {
            "id": 18,
            "name": "Buffer",
            "omniauth_class": "bsbuffer",
            "slug": "buffer"
          },
          "value_is_set": false
        }
      ],
      "organization_id": null,
      "parameters": [],
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
          "profiles": {}
        },
        "title": "profiles-information-buffer",
        "type": "object"
      },
      "secrets": [],
      "tag": {
        "description": "Buffer is a software application designed to manage social networks, by providing the means for a user to schedule posts to Twitter, Facebook, and Linkedin.",
        "full_image_url": "https://static.blockspring.com/tag-icons/buffer.png",
        "id": 382,
        "image_url": "buffer.png",
        "name": "buffer",
        "oauth": [
          {
            "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=get-user-info-buffer",
            "id": 141,
            "provider": {
              "id": 18,
              "name": "Buffer",
              "omniauth_class": "bsbuffer",
              "slug": "buffer"
            },
            "value_is_set": false
          }
        ],
        "readable_name": "Buffer",
        "secrets": [],
        "url": "https://api.blockspring.com/v0/tags/382?access_token={access_token}"
      },
      "title": "Get Info on Your Buffer Social Profiles",
      "updated_at": 1442203153,
      "url": "https://api.blockspring.com/v0/blocks/profiles-information-buffer?access_token={access_token}",
      "username": "bs",
      "uuid": "8386bc59296644b110c84e27d4e543e7"
    },
    {
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
      "created_at": 1439425248,
      "description": "Get updates sent for a social media profile on Buffer. Includes (if available) share statistics of your social media updates such as views, favorites, re-shares.",
      "favorite_url": "https://api.blockspring.com/v0/favorites/sent-updates-buffer?access_token={access_token}",
      "formatted_tag_line": "Get updates (content and analytics) sent for a social media profile on Buffer",
      "html_description": "<p>Get updates sent for a social media profile on Buffer. Includes (if available) share statistics of your social media updates such as views, favorites, re-shares.</p>\n",
      "id": "sent-updates-buffer",
      "is_favorited": false,
      "is_imported_to_organization": false,
      "is_open_source": true,
      "is_public": true,
      "oauth": [
        {
          "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=sent-updates-buffer",
          "id": 141,
          "provider": {
            "id": 18,
            "name": "Buffer",
            "omniauth_class": "bsbuffer",
            "slug": "buffer"
          },
          "value_is_set": false
        }
      ],
      "organization_id": null,
      "parameters": [
        {
          "default": "",
          "help_text": "Find your social profile IDs here: https://open.blockspring.com/blocks/profiles-information-buffer.",
          "label": "Profile ID",
          "name": "profile_id",
          "optional": false,
          "type": "text"
        },
        {
          "default": "1",
          "help_text": "Return a specific page of results.",
          "label": "Page",
          "name": "page",
          "optional": true,
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
        "title": "sent-updates-buffer",
        "type": "object"
      },
      "secrets": [],
      "tag": {
        "description": "Buffer is a software application designed to manage social networks, by providing the means for a user to schedule posts to Twitter, Facebook, and Linkedin.",
        "full_image_url": "https://static.blockspring.com/tag-icons/buffer.png",
        "id": 382,
        "image_url": "buffer.png",
        "name": "buffer",
        "oauth": [
          {
            "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=get-user-info-buffer",
            "id": 141,
            "provider": {
              "id": 18,
              "name": "Buffer",
              "omniauth_class": "bsbuffer",
              "slug": "buffer"
            },
            "value_is_set": false
          }
        ],
        "readable_name": "Buffer",
        "secrets": [],
        "url": "https://api.blockspring.com/v0/tags/382?access_token={access_token}"
      },
      "title": "Get Sent Updates from Buffer",
      "updated_at": 1442207022,
      "url": "https://api.blockspring.com/v0/blocks/sent-updates-buffer?access_token={access_token}",
      "username": "bs",
      "uuid": "f2a72ac5986a06048aa138a2ef4bd023"
    }
  ],
  "description": "Buffer is a software application designed to manage social networks, by providing the means for a user to schedule posts to Twitter, Facebook, and Linkedin.",
  "full_image_url": "https://static.blockspring.com/tag-icons/buffer.png",
  "id": 382,
  "image_url": "buffer.png",
  "name": "buffer",
  "oauth": [
    {
      "auth_url": "https://auth.blockspring.com/users/auth/bsbuffer?api_key={access_token}&via=sheets&block=get-user-info-buffer",
      "id": 141,
      "provider": {
        "id": 18,
        "name": "Buffer",
        "omniauth_class": "bsbuffer",
        "slug": "buffer"
      },
      "value_is_set": false
    }
  ],
  "readable_name": "Buffer",
  "secrets": [],
  "url": "https://api.blockspring.com/v0/tags/382?access_token={access_token}"
}
```
