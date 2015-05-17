# Stages

## Get stages

> Sample request

```shell
curl -X GET "http://example.com/api/v1/stages" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"checklist_id": 1}'
```

> Sample response

```json
{
  "status": 200,
  "data": [
    {
      "id": 1,
      "number": 1,
      "name": "First stage"
    },
    {
      "id": 2,
      "number": 2,
      "name": "Second stage"
    },
    {
      "id": 3,
      "number": 3,
      "name": "Last stage"
    }
  ]
}
```
This endpoint gets all available stages for a checklist

### HTTP Request

`GET http://example.com/api/v1/stages`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
checklist_id | required | |
