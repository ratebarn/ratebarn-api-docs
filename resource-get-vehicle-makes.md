#### Get Vehicle Makes
```
GET /api/v1/vehicle_makes
```


*Returns list of vehicle makes*

## Pagination 

Use the field *paginate* to toggle pagination off or on. Use paginate="true" to enable or paginate="false" to disable pagination.

###### Example

```bash
curl -X GET \
  https://gosavvy.io/api/v1/vehicle_makes \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {**YOUR-ACCESS-TOKEN**}' \
  -d ''
```


```javascript
{
  "data": [
    {
      //VEHICLE MAKE OBJECT 1..
    },
    {
      //VEHICLE MAKE OBJECT 2..
    }
    //etc...
  ],
  "links": {
    "first": "http:\/\/homestead.test\/api\/v1\/vehicle_makes?page=1",
    "last": "http:\/\/homestead.test\/api\/v1\/vehicle_makes?page=2",
    "prev": null,
    "next": "http:\/\/homestead.test\/api\/v1\/vehicle_makes?page=2"
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 2,
    "path": "http:\/\/homestead.test\/api\/v1\/vehicle_makes",
    "per_page": 15,
    "to": 15,
    "total": 30
  }
}
```
