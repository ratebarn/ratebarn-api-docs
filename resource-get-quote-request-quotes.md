#### Get Quote Request Quotes
```
GET /api/v1/quote_requests/{quote_request_id}/quotes
```

*Returns all connected quote request's quotes models*

## Pagination 

Use the field *paginate* to toggle pagination off or on. Use paginate="true" to enable or paginate="false" to disable pagination.

###### Example

```bash
curl -X GET \
  https://gosavvy.io/api/v1/quote_requests/{QUOTE_REQUEST_ID}/quotes \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {**YOUR-ACCESS-TOKEN**}' \
  -d ''
```

```javascript
{
  "data": [
    {
      //QUOTE OBJECT 1..
    },
    {
      //QUOTE OBJECT 2..
    }
    //etc...
  ],
  "links": {
    "first": "http:\/\/homestead.test\/api\/v1\/quote_requests1\/1\/quotes?page=1",
    "last": "http:\/\/homestead.test\/api\/v1\/quote_requests\/1\/quotes?page=2",
    "prev": null,
    "next": "http:\/\/homestead.test\/api\/v1\/quote_requests\/1\/quotes?page=2"
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 2,
    "path": "http:\/\/homestead.test\/api\/v1\/quote_requests\/1\/quotes",
    "per_page": 15,
    "to": 15,
    "total": 30
  }
}
```
