# Car types

## Get car types

> Sample request

```shell
curl -X GET "http://example.com/api/v1/car_types" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": [
    {
      "id": 1,
      "car_model_id": 1,
      "name": "BMW-X6",
      "created_at": "2015-05-16T16:38:14.000Z",
      "updated_at": "2015-05-16T16:38:54.000Z"
    },
    {
      "id": 2,
      "car_model_id": 2,
      "name": "audi-A8",
      "created_at": "2015-05-16T16:39:26.000Z",
      "updated_at": "2015-05-16T16:39:26.000Z"
    }
  ]
}
```
This endpoint gets all types of car

### HTTP Request

`GET http://example.com/api/v1/car_types`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
