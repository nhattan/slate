# Tasks

## Get tasks

> Sample request

```shell
curl -X GET "http://example.com/api/v1/tasks" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token": "some_token"}'
```

> Sample response

```json
{
  "data": {
    "tasks": [
      {
        "id": 4,
        "type": "website",
        "name": "Removal quote task (displayed)",
        "days": -60,
        "description": "Removal quote task DESCRIPTION",
        "button_label": "Removal quote task LABEL",
        "done": true,
        "overdue": false,
        "link": "/quotes/new/4"
      },
      {
        "id": 5,
        "type": "website",
        "name": "Conveyancer quote task (displayed)",
        "days": -60,
        "description": "Conveyancer quote task DESCRIPTION",
        "button_label": "Conveyancer quote task LABEL",
        "done": true,
        "overdue": false,
        "link": "/quotes/new/5"
      },
      {
        "id": 3,
        "type": "inform",
        "name": "Inform task (displayed)",
        "days": -45,
        "description": "Inform task DESCRIPTION",
        "button_label": "Inform task LABEL",
        "done": true,
        "overdue": false,
        "message": "Custom Inform Message",
        "destinations": [
          {
              "name": "Company 1",
              "id": 1,
              "address": "",
              "telephone": "111111111",
              "link_label": "Information 1",
              "link": "http://www.company-url-1.com"
          },
          {
              "name": "Company 2",
              "id": 2,
              "address": "",
              "telephone": "111111112",
              "link_label": "Information 2",
              "link": "http://www.company-url-2.com"
          },
          {
              "name": "Company 3",
              "id": 3,
              "address": "",
              "telephone": "111111113",
              "link_label": "Information 3",
              "link": "http://www.company-url-3.com"
          }
        ]
      },
      {
        "id": 2,
        "type": "website",
        "name": "Website task (displayed)",
        "days": -30,
        "description": "Website task DESCRIPTION",
        "button_label": "Website task LABEL",
        "done": false,
        "overdue": true
      },
      {
        "id": 1,
        "type": "document",
        "name": "Document task (displayed)",
        "days": -15,
        "description": "Document task DESCRIPTION",
        "button_label": "Document task LABEL",
        "done": false,
        "overdue": false
      }
    ]
  }
}
```
This endpoint retrieve all tasks with status information

### HTTP Request

`GET http://example.com/api/v1/tasks`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
auth_token | required | | auth_token received when signing in user



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
      "description": "Document task DESCRIPTION",
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
