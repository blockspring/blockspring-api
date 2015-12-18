# Organizations

1. [Get Organization Info](#get-organization-info)
2. [Get Organization Tags](#get-organization-tags)

## Get Organization Info

Get information about the current user's organization.

### Endpoint

`GET /v0/organization`

### Parameters

None

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

```javascript
{
    "name": "Acme, Inc",
    "subdomain": "acme-inc"
}
```

## Get Organization Tags

Get a list of the current organization's tags.

### Endpoint

`GET /v0/organization/tags`

### Parameters

None

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

Response format is the same as the [official tags endpoint](/v0/tags#list-tags)
