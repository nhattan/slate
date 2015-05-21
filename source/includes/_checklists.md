# Checklists

## Get checklists

> Sample request

```shell
curl -X GET "http://example.com/api/v1/checklists" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": [
    {
      "id": 1,
      "white_label_id": 1,
      "name": "Check list",
      "display_name": "Check list for a student",
      "created_at": "2015-05-04T15:25:31.000Z",
      "updated_at": "2015-05-04T15:25:31.000Z",
      "all_countries": true
    }
  ]
}
```
This endpoint gets all available checklists

### HTTP Request

`GET http://example.com/api/v1/checklists`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
