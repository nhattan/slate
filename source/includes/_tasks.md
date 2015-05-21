# Tasks

## Get tasks

> Sample request

```shell
curl -X GET "http://example.com/api/v1/tasks" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
    "success": 200,
    "data": [
        {
            "id": 4,
            "type": "website",
            "name": "Removal quote task (displayed)",
            "days": -60,
            "description": "Removal quote task DESCRIPTION",
            "button_label": "Removal quote task LABEL",
            "done": false,
            "overdue": true,
            "link": "/quotes/new/4"
        },
        {
            "id": 5,
            "type": "website",
            "name": "Conveyancer quote task (displayed)",
            "days": -60,
            "description": "Conveyancer quote task DESCRIPTION",
            "button_label": "Conveyancer quote task LABEL",
            "done": false,
            "overdue": true,
            "link": "/quotes/new/5"
        },
        {
            "id": 3,
            "type": "inform",
            "name": "Inform task (displayed)",
            "days": -45,
            "description": "Inform task DESCRIPTION",
            "button_label": "Inform task LABEL",
            "done": false,
            "overdue": true,
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
            "overdue": true
        }
    ]
}
```
This endpoint gets all tasks with status information

### HTTP Request

`GET http://example.com/api/v1/tasks`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## Get tasks by weeks

> Sample request

```shell
curl -X GET "http://example.com/api/v1/weeks" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": [
    {
      "position": 0,
      "number": 0,
      "overdue": true,
      "start_date": null,
      "end_date": "2015-05-10",
      "tasks": [
        {
          "id": 4,
          "type": "website",
          "name": "Removal quote task (displayed)",
          "days": -60,
          "description": "Removal quote task DESCRIPTION",
          "button_label": "Removal quote task LABEL",
          "done": false,
          "overdue": true,
          "link": "/quotes/new/4"
        },
        {
          "id": 5,
          "type": "website",
          "name": "Conveyancer quote task (displayed)",
          "days": -60,
          "description": "Conveyancer quote task DESCRIPTION",
          "button_label": "Conveyancer quote task LABEL",
          "done": false,
          "overdue": true,
          "link": "/quotes/new/5"
        },
        {
          "id": 3,
          "type": "inform",
          "name": "Inform task (displayed)",
          "days": -45,
          "description": "Inform task DESCRIPTION",
          "button_label": "Inform task LABEL",
          "done": false,
          "overdue": true,
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
          "overdue": true
        }
      ]
    }
  ]
}
```

This endpoint gets list of tasks by weeks

### HTTP Request

`GET http://example.com/api/v1/weeks`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## Get task details

> Sample request

```shell
curl -X GET "http://example.com/api/v1/tasks/1" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "id": 1,
    "type": "document",
    "name": "Document task (displayed)",
    "days": -15,
    "description": "Document task DESCRIPTION",
    "button_label": "Document task LABEL",
    "done": false
  }
}
```
This endpoint gets details of a task

### HTTP Request

`GET http://example.com/api/v1/tasks/:id`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## Mark a task as done or todo

> Sample request

```shell
curl -X POST "http://example.com/api/v1/task/1/update" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"type": "todo"}'

```

> Sample response

```json
{
  "success": 200,
  "data": {
    "id": 1,
    "type": "document",
    "name": "Document task (displayed)",
    "days": -15,
    "description": "Document task DESCRIPTION",
    "button_label": "Document task LABEL",
    "done": false
  }
}
```

This endpoint marks a task as done or todo

### HTTP Request

`POST http://example.com/api/v1/tasks/:id/update`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
type | required | | "done" or "todo"



## Create document, generic planner

> Sample request

```shell
curl -X POST "http://example.com/api/v1/task/1/document" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"title": "Mr", "first_name": "David", "last_name": "Black", "phone_1": "324234234", "move_date": "2014/05/06", "from_postcode": "MK5 8FT", "from_address_line_1": "address 1", "from_address_line_2": "address 2", "from_town": "my town", "from_county": "my county", "provider_name": "Provider 1", "provider_postcode": "MK5 8FT", "provider_address_line_1": "provider address 1", "provider_address_line_2": "provider address 2", "provider_town": "provider town", "provider_county": "provider county"}'

```

> Sample response

```
Status: 200
Content-type: application/pdf
```

This endpoint creates a document for a document task, generic planner

### HTTP Request

`POST http://example.com/api/v1/tasks/:id/document`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
title | optional | |
first_name | optional | |
last_name | optional | |
phone_1 | optional | |
move_date | optional | |
from_postcode | optional | |
from_address_line_1 | optional | |
from_address_line_2 | optional | |
from_town | optional | |
from_county | optional | |
provider_name | optional | |
provider_postcode | optional | |
provider_address_line_1 | optional | |
provider_address_line_2 | optional | |
provider_town | optional | |
provider_county | optional | |
