# Block Execution

Executing blocks is as easy as making a `POST` request to `https://run.blockspring.com/api_v2/blocks/:block_id`.

## Sample Execution

To run the `math` block, make a request like so:

```bash
curl -H "Content-Type: application/json" -d "{ \"expression\": \"3+3\" }" "https://run.blockspring.com/api_v2/blocks/math?api_key={access_token}"
```

Pass the user's access token which can be acquired via our [OAuth flow](/authentication.md#authentication).

## Sample Response

```http
Status: 200 OK
X-Blockspring-Exit-Code: 0
X-Blockspring-RateLimit-Limit: 100000
X-Blockspring-RateLimit-Remaining: 99975
X-Blockspring-RateLimit-Reset: 1450401604
X-Blockspring-Response-Time: 88
X-Blockspring-Run-ID: 6960f7f7a534e4d77fcef8d633bfe837
```
```javascript
{
  "_blockspring_spec": true,
  "_errors": [],
  "result": 6
}
```


## Error responses

### Graceful errors

Graceful errors are errors that the block creator caught and reacted to. These errors will be located in the array `_errors`.

#### Sample Request

```bash
curl -H "Content-Type: application/json" -d "{ \"email\": \"paul@blockspring.com\" }" "https://run.blockspring.com/api_v2/blocks/invite-blockspring-slack?api_key={access_token}"
```

#### Sample Response

```http
Status: 200 OK
X-Blockspring-Exit-Code: 0
X-Blockspring-RateLimit-Limit: 100000
X-Blockspring-RateLimit-Remaining: 99996
X-Blockspring-RateLimit-Reset: 1450402207
X-Blockspring-Response-Time: 394
X-Blockspring-Run-ID: 6960f7f7a534e4d77fcef8d633bfe837
```
```javascript
{
  "_blockspring_spec": true,
  "_errors": [
    {
      "title" : "Slack error",
      "message" : "already_in_team"
    }
  ]
}
```


### Runtime Errors

While rare, it is possible for a runtime error to occur. In this case, the HTTP status code will not be a `200` and the `X-Blockspring-Exit-Code` header will be non-zero.

#### Sample Error Response

```http
Status: 500 Internal Server Error
X-Blockspring-Exit-Code: 1
X-Blockspring-RateLimit-Limit: 100000
X-Blockspring-RateLimit-Remaining: 99981
X-Blockspring-RateLimit-Reset: 1450402207
X-Blockspring-Response-Time: 256
X-Blockspring-Run-ID: 23e2e8e5a8c5c4820d947f8e97d30315
```
```
pyparsing.ParseException: Expected end of text (at char 1), (line:1, col:2)
```
