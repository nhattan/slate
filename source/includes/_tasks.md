# Tasks

## Get task details

> Sample request

```shell
curl -X GET "http://example.com/api/v1/tasks" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token": "some_token"}'
```

> Sample response

```json
{
  "data": {
    "task": {
      "id": 1,
      "type": "document",
      "name": "Document task (displayed)",
      "days": -15,
      "description": "Document task DESCRIPTION,
      "button_label": "Document task LABEL",
      "done": false
    }
  }
}
```
This endpoint retrieve details of a task

### HTTP Request

`GET http://example.com/api/v1/tasks/:id`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
id | required | | Required into the URL
auth_token | required | | auth_token received when signing in user
