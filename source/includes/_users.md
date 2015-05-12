# Users

## Get user

> Sample request

```shell
curl -X GET "http://example.com/api/v1/users" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token": "some_token"}'
```

> Sample response

```json
{
  "data": {
      "user": {
          "id": 1,
          "email": "nhattan@gmail.com",
          "created_at": "2015-04-21T03:28:46.000Z",
          "updated_at": "2015-04-21T08:58:39.636Z",
          "accept_terms": true,
          "opt_in_retention": true,
          "opt_in_acquisition": true,
          "title": "Mr",
          "first_name": "Tan",
          "last_name": "Nguyen",
          "phone_1": null,
          "phone_2": null,
          "white_label_id": 1,
          "authentication_token": "some_token",
          "auto_registered": null,
          "standard_password": null,
          "registration_token": null,
          "optout": null,
          "legacy_id": null,
          "marketing_permissions_rev": null,
          "opt_out_retention": false,
          "photo": {
              "url": null,
              "thumb": {
                  "url": null
              }
          }
      }
  }
}
```

This endpoint retrieves current user.

### HTTP Request

`GET http://example.com/api/v1/users`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
auth_token | required | | auth_token received when signing in user



## User registration

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"email":"nhattan@gmail.com","password":"12345678","password_confirmation":"12345678","accept_terms":1,"opt_in_retention":1,"opt_in_acquisition":1,"title":"Mr","first_name":"Tan","last_name":"Nguyen","phone_1":"1693625484","move_date":"2014/05/06","from_postcode":"MK5 8FT","from_address_line_1":"address 1","from_address_line_2":"address 2","from_town":"Tran Phu","from_county":"Ba Dinh"}'
```

> Sample response

```json
{
  "data": {
      "user": {
        "authentication_token": "some_token"
      }
  }
}
```

This endpoint create a user then signin it.

### HTTP Request

`POST http://example.com/api/v1/users`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
email | required | |
password | required | |
password_confirmation | required | |
accept_terms | required | | 1 = accept terms
opt_in_retention | optional | | 1 = will endeavour to update companies that already have your contact information with your new home details
opt_in_acquisition | optional | | 1 = will keep you updated with news, advice, special offers and services related to my home move from selected third parties by email and otherforms of communication
title | optional | | ex. Mr
first_name | optional | |
last_name | optional | |
phone_1 | optional | |
move_date | optional | | ending date
from_postcode | optional | |
from_address_line_1 | optional | |
from_address_line_2 | optional | |
from_town | optional | |
from_county | optional | |



## Update user

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/update" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token":"some_token",email":"nhattan@gmail.com","password":"12345678","password_confirmation":"12345678","accept_terms":1,"opt_in_retention":1,"opt_in_acquisition":1,"title":"Mr","first_name":"Tan","last_name":"Nguyen","phone_1":"1693625484","move_date":"2014/05/06","from_postcode":"MK5 8FT","from_address_line_1":"address 1","from_address_line_2":"address 2","from_town":"Tran Phu","from_county":"Ba Dinh"}'
```

> Sample response

```json
{
  "data": {
    "user": {
      "id": 35,
      "email": "nhattan@gmail.com",
      "created_at": "2015-05-11T04:01:00.000Z",
      "updated_at": "2015-05-11T06:36:28.608Z",
      "accept_terms": true,
      "opt_in_retention": true,
      "opt_in_acquisition": true,
      "title": "Mr",
      "first_name": "Tan",
      "last_name": "Nguyen",
      "phone_1": "1693625484",
      "phone_2": null,
      "white_label_id": 1,
      "authentication_token": "some_token",
      "auto_registered": null,
      "standard_password": null,
      "registration_token": null,
      "optout": null,
      "legacy_id": null,
      "marketing_permissions_rev": null,
      "opt_out_retention": false,
      "photo": {
        "url": null,
        "thumb": {
          "url": null
        }
      }
    }
  }
}
```

This endpoint update a user.

### HTTP Request

`POST http://example.com/api/v1/users/update`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
email | required | |
password | required | |
password_confirmation | required | |
accept_terms | required | | 1 = accept terms
opt_in_retention | optional | | 1 = will endeavour to update companies that already have your contact information with your new home details
opt_in_acquisition | optional | | 1 = will keep you updated with news, advice, special offers and services related to my home move from selected third parties by email and otherforms of communication
title | optional | | ex. Mr
first_name | optional | |
last_name | optional | |
phone_1 | optional | |
move_date | optional | | ending date
from_postcode | optional | |
from_address_line_1 | optional | |
from_address_line_2 | optional | |
from_town | optional | |
from_county | optional | |



## User sign in

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/sign_in" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"email":"nhattan@gmail.com","password":"12345678"}'
```

> Sample response

```json
{
  "data": {
      "user": {
          "email": "nhattan@gmail.com",
          "accept_terms": true,
          "authentication_token": "some_token"
      }
  }
}
```

This endpoint sign in a user

### HTTP Request

`POST http://example.com/api/v1/users/sign_in`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
email | required | |
password | required | |


## User sign out

> Sample request

```shell
curl -X DELETE "http://example.com/api/v1/users/sign_out" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token":"some_token"}'
```

> Sample response

```json
{
  "data": {}
}
```

This endpoint sign out a user

### HTTP Request

`DELETE http://example.com/api/v1/users/sign_out`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
email | required | |
auth_token | required | |


## Get custom fields

> Sample request

```shell
curl -X GET "http://example.com/api/v1/users/custom_fields" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow'
```

> Sample response

```json
{
  "data": {
    "custom_fields": [
      {
        "name": "field_have_you_got_a_garden",
        "label": "have_you_got_a_garden",
        "input_type": "checkbox",
        "required": true,
        "options": []
      },
      {
        "name": "field_alternative_name",
        "label": "alternative_name",
        "input_type": "input",
        "required": false,
        "options": []
      },
      {
        "name": "field_number_of_children",
        "label": "number_of_children",
        "input_type": "radio",
        "required": true,
        "options": [
          [
            "Yes",
            "yes"
          ],
          [
            "no",
            "no"
          ]
        ]
      },
      {
        "name": "field_birthday",
        "label": "birthday",
        "input_type": "date",
        "required": true,
        "options": []
      },
      {
        "name": "field_rate_us",
        "label": "rate_us",
        "input_type": "select",
        "required": false,
        "options": [
            [
              "Poor",
              "poor"
            ],
            [
              "Good",
              "good"
            ],
            [
              "Excellent",
              "excellent"
            ]
        ]
      },
      {
        "name": "field_comment",
        "label": "comment",
        "input_type": "textarea",
        "required": false,
        "options": []
      }
    ]
  }
}
```

This endpoint retrieves all user custom fields

### HTTP Request

`GET http://example.com/api/v1/users/custom_fields`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
