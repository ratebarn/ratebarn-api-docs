#### Get Quote Requests
```
GET /api/v1/quote_requests
```

*Returns all connected quote request models*

## Pagination 

Use the field *paginate* to toggle pagination off or on. Use paginate="true" to enable or paginate="false" to disable pagination.

###### Example

```bash
curl -X GET \
  https://gosavvy.io/api/v1/quote_requests \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {**YOUR-ACCESS-TOKEN**}' \
  -d ''
```


```javascript
{
  "data": [
    {
      //QUOTE REQUEDST OBJECT 1..
    },
    {
      //QUOTE REQUEDST OBJECT 2..
    }
    //etc...
  ],
  "links": {
    "first": "http:\/\/homestead.test\/api\/v1\/quote_requests?page=1",
    "last": "http:\/\/homestead.test\/api\/v1\/quote_requests?page=2",
    "prev": null,
    "next": "http:\/\/homestead.test\/api\/v1\/quote_requests?page=2"
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 2,
    "path": "http:\/\/homestead.test\/api\/v1\/quote_requests",
    "per_page": 15,
    "to": 15,
    "total": 30
  }
}
```
