# Instructors

## Get intructor

> Sample request

```shell
curl -X GET "http://example.com/api/v1/intructor/tran-thanh"-H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow'
```

> Sample response

```json
{
  "data": {
    "instructor": {
      "table": {
        "slug": "tran-thanh",
        "first_name": "Tran",
        "last_name": "Thanh",
        "description": null,
        "driving_school_name": "",
        "teaching_since": null,
        "testimonials_count": null,
        "user_rating": 0,
        "gender": "M",
        "location": {
            "name": "Tran phu, Ha Noi",
            "postcode": "5c8e62",
            "range_km": null,
            "lat": 51.915862,
            "lon": -0.64369
        },
        "coverage": [],
        "avatar": {
            "url": "/assets/fallback/avatar/default-a3fa46ca7933dd2767c4b22d4c5034e9.jpg",
            "standard": {
                "url": "/assets/fallback/avatar/standard_default-3520b3d59ecb0207c53df02ff132805a.jpg"
            },
            "thumb": {
                "url": "/assets/fallback/avatar/thumb_default-c2e90a06644af95aa4c2e3f8a35d2490.jpg"
            }
        },
        "images": [],
        "services": [],
        "best_price": 0,
        "best_one_hour_price": 1,
        "languages": [],
        "qualifications": [
            "Drive iQ Pro"
        ],
        "affiliations": [],
        "specialities": [],
        "verified": false
      },
      "modifiable": true
    }
  }
}
```
This endpoint retrieve all info of a instructor

### HTTP Request

`GET http://example.com/api/v1/instructors/:slug`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
