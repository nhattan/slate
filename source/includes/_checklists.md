# Checklists

## Get checklists

> Sample request

```shell
curl -X GET "http://example.com/api/v1/checklists" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow'
```

> Sample response

```json
{
  "data": {
    "checklists": [
      {
        "id": 1,
        "white_label_id": 1,
        "name": "Check list",
        "display_name": "Check list for a student",
        "created_at": "2015-05-05T03:51:42.000Z",
        "updated_at": "2015-05-05T03:51:42.000Z",
        "all_countries": true
      }
    ]
  }
}
```
This endpoint retrieve all available checklists

### HTTP Request

`GET http://example.com/api/v1/checklists`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
