# Car types

## Get car types

> Sample request

```shell
curl -X GET "http://example.com/api/v1/car_types" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow'
```

> Sample response

```json
{
  "data": {
    "car_types": [
      {
        "id": 1,
        "car_model_id": 2,
        "name": "BMW-X6",
        "created_at": "2015-02-10T14:35:44.000Z",
        "updated_at": "2015-05-18T14:36:00.000Z"
      },
      {
        "id": 2,
        "car_model_id": 3,
        "name": "audi-A8 ",
        "created_at": "2015-05-15T16:30:49.000Z",
        "updated_at": "2015-05-15T16:30:53.000Z"
      }
    ]
  }
}
```
This endpoint list all car types

### HTTP Request

`GET http://example.com/api/v1/car_types`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
auth_token | required | | auth_token received when signing in user
