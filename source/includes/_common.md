# Common

## Get progress

> Sample request

```shell
curl -X GET "http://example.com/api/v1/progress" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token": "some_token"}'
```

> Sample response

```json
{
  "data": {
    "progress": {
      "progress_percentage": 60,
      "tasks_count": 5,
      "tasks_done_count": 3,
      "tasks_todo_count": 2,
      "tasks_overdue_count": 5,
      "days_left_to_move": 11
    }
  }
}
```
This endpoint get progress info

### HTTP Request

`GET http://example.com/api/v1/progress`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
auth_token | required | | auth_token received when signing in user



## Get addresses

> Sample request

```shell
curl -X GET "http://example.com/api/v1/addresses" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"postcode": "MK5 8FT"}'
```

> Sample response

```json
{
  "data": {
    "addresses": [
      {
        "Udprn": "50737582",
        "Company": "Baker Small Solicitors",
        "Department": "",
        "Line1": "2 Whittle Court",
        "Line2": "Knowlhill",
        "Line3": "",
        "Line4": "",
        "Line5": "",
        "PostTown": "Milton Keynes",
        "County": "Buckinghamshire",
        "Postcode": "MK5 8FT",
        "Mailsort": "47136",
        "Barcode": "(MK58FT1AL)",
        "Type": "SmallBusiness",
        "DeliveryPointSuffix": "1A",
        "SubBuilding": "",
        "BuildingName": "",
        "BuildingNumber": "2",
        "PrimaryStreet": "Whittle Court",
        "SecondaryStreet": "",
        "DoubleDependentLocality": "",
        "DependentLocality": "Knowlhill",
        "PoBox": "",
        "CountryName": "England"
      },
      {
        "Udprn": "50737587",
        "Company": "Twenty C I Ltd",
        "Department": "",
        "Line1": "6 Whittle Court",
        "Line2": "Knowlhill",
        "Line3": "",
        "Line4": "",
        "Line5": "",
        "PostTown": "Milton Keynes",
        "County": "Buckinghamshire",
        "Postcode": "MK5 8FT",
        "Mailsort": "47136",
        "Barcode": "(MK58FT1GR)",
        "Type": "SmallBusiness",
        "DeliveryPointSuffix": "1G",
        "SubBuilding": "",
        "BuildingName": "",
        "BuildingNumber": "6",
        "PrimaryStreet": "Whittle Court",
        "SecondaryStreet": "",
        "DoubleDependentLocality": "",
        "DependentLocality": "Knowlhill",
        "PoBox": "",
        "CountryName": "England"
      }
    ]
  }
}
```

This endpoint get the list of all the addresses for a postcode

### HTTP Request

`GET http://example.com/api/v1/addresses`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
postcode | required | |
