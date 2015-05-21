# Common

## Get progress

> Sample request

```shell
curl -X GET "http://example.com/api/v1/progress" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "progress_percentage": 0,
    "tasks_count": 5,
    "tasks_done_count": 0,
    "tasks_todo_count": 5,
    "tasks_overdue_count": 5,
    "days_left_to_move": -376
  }
}
```
This endpoint get progress info

### HTTP Request

`GET http://example.com/api/v1/progress`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## Get addresses

> Sample request

```shell
curl -X GET "http://example.com/api/v1/addresses" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"postcode": "MK5 8FT"}'
```

> Sample response

```json
{
  "success": 200,
  "data": [
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
```

This endpoint gets the list of all the addresses for a postcode

### HTTP Request

`GET http://example.com/api/v1/addresses`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
postcode | required | |
