# Users

## Get user

> Sample request

```shell
curl -X GET "http://example.com/api/v1/users" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "title": "Mr",
    "first_name": "David",
    "phone_1": "01693625484",
    "from_postcode": "MK5 8FT",
    "from_address_line_1": "address 1",
    "from_address_line_2": "address 2",
    "from_town": "my town",
    "from_county": "my county",
    "move_date": "2014-05-06",
    "field_have_you_got_a_garden": false,
    "field_alternative_name": "David Black",
    "field_birthdate": "1992-05-30",
    "field_rate_us": 2,
    "field_are_you_sure": "no"
  }
}
```

This endpoint gets current user

### HTTP Request

`GET http://example.com/api/v1/users`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## User registration

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"email": "davidblack@gmail.com", "password": "12345678", "password_confirmation": "12345678", "accept_terms": 1, "opt_in_retention": 1, "opt_in_acquisition": 1, "title": "Mr", "first_name": "David", "last_name": "Black", "phone_1": "1693625484", "move_date": "2014/05/06", "from_postcode": "MK5 8FT", "from_address_line_1": "address 1", "from_address_line_2": "address 2", "from_town": "my town", "from_county": "my county", "field_have_you_got_a_garden": false, "field_alternative_name": "David", "field_birthdate": "1992-05-30", "field_rate_us": 2,
"field_are_you_sure": "no"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "email": "davidblack@gmail.com",
    "accept_terms": true,
    "authentication_token": "some_token"
  }
}
```

This endpoint creates a user then sign user in

### HTTP Request

`POST http://example.com/api/v1/users`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
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
field_have_you_got_a_garden | optional | | custom field
field_alternative_name | optional | | custom field
field_birthdate | optional | | custom field
field_rate_us | optional | | custom field
field_are_you_sure | optional | | custom field



## Update user

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/update" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"email": "nhattan@gmail.com", "password": "12345678", "password_confirmation": "12345678", "accept_terms": 1, "opt_in_retention": 1, "opt_in_acquisition": 1, "title": "Mr", "first_name": "Tan", "last_name": "Nguyen", "phone_1": "1693625484", "move_date": "2014/05/06", "from_postcode": "MK5 8FT", "from_address_line_1": "address 1", "from_address_line_2": "address 2", "from_town": "my town", "from_county": "my county"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "title": "Mr",
    "first_name": "David",
    "phone_1": "01693625484",
    "from_postcode": "MK5 8FT",
    "from_address_line_1": "address 1",
    "from_address_line_2": "address 2",
    "from_town": "my town",
    "from_county": "my county",
    "move_date": "2014-05-06",
    "field_have_you_got_a_garden": false,
    "field_alternative_name": "David Black",
    "field_birthdate": "1992-05-30",
    "field_rate_us": 2,
    "field_are_you_sure": "no"
  }
}
```

This endpoint updates a user

### HTTP Request

`POST http://example.com/api/v1/users/update`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
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
field_have_you_got_a_garden | optional | | custom field
field_alternative_name | optional | | custom field
field_birthdate | optional | | custom field
field_rate_us | optional | | custom field
field_are_you_sure | optional | | custom field



## User sign in

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/sign_in" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"email":"davidblack@gmail.com","password":"12345678"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "email": "davidblack@gmail.com",
    "accept_terms": true,
    "authentication_token": "some_token"
  }
}
```

This endpoint signs in a user

### HTTP Request

`POST http://example.com/api/v1/users/sign_in`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
email | required | |
password | required | |



## User sign out

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/sign_out" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```

This endpoint signs out a user

### HTTP Request

`POST http://example.com/api/v1/users/sign_out`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
email | required | |



## Get custom fields

> Sample request

```shell
curl -X GET "http://example.com/api/v1/users/custom_fields" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": [
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
```

This endpoint gets all user custom fields

### HTTP Request

`GET http://example.com/api/v1/users/custom_fields`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
