# Instructors

## Get instructor

> Sample request

```shell
curl -X GET "http://example.com/api/v1/instructors/tran-thanh"-H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof'
```

> Sample response

```json
{
  "success": 200,
  "data": {
    "table": {
      "slug": "tran-thanh",
      "first_name": "Tran",
      "last_name": "Thanh",
      "description": "We are a no nonsense driving school and will have you on the road asap. Very flexible with times as we understand people lead a busy lifestyle these days. \r\nFirst lesson is £11 this is for you to see if your comfortable with the instructor and wish to carry on. \r\nAll services provided with pass plus motorway driving etc. \r\nCar is renewed every 18 months and is air conditioned.\r\nLessons can be as long or as short as you desire with prices to match length of the lesson you choose. \r\nText, email or simply phone to book your lesson now!",
      "driving_school_name": "Atomdrivingschool@btinternet.com",
      "teaching_since": "2001-09-01T00:00:00+01:00",
      "testimonials_count": null,
      "user_rating": 0,
      "gender": "M",
      "location": {
        "name": "Leighton Buzzard, United Kingdom",
        "postcode": "Lu73lz",
        "range_km": null,
        "lat": 51.919684,
        "lon": -0.660657
      },
      "coverage": [
        "LU7",
        "MK17",
        "MK2",
        "LU6",
        "LU5",
        "MK3",
        "MK1",
        "MK7",
        "MK4",
        "LU4",
        "MK6",
        "MK10",
        "HP23",
        "MK5",
        "MK9",
        "HP22",
        "HP20",
        "LU3",
        "HP19",
        "MK15",
        "MK8",
        "HP21",
        "LU1",
        "MK45",
        "MK13",
        "MK14",
        "MK77",
        "HP4",
        "LU2",
        "MK12"
      ],
      "avatar": {
        "url": "/assets/fallback/avatar/default-a3fa46ca7933dd2767c4d4c5034e9.jpg",
        "standard": {
          "url": "/assets/fallback/avatar/standard_default-3520b3d59ecb0207cf02ff132805a.jpg"
        },
        "thumb": {
          "url": "/assets/fallback/avatar/thumb_default-c2e90a066445aa4c2e3f8a35d2490.jpg"
        }
      },
      "images": [],
      "services": [
        {
          "id": 405,
          "name": "Standard Lesson",
          "icon": "learner.png",
          "discount_name": null,
          "length_mins": 60,
          "price_cents": 2200,
          "price": "£22.00",
          "min_purchase": 1
        },
        {
          "id": 406,
          "name": "Intensive courses",
          "icon": "intensive.png",
          "discount_name": null,
          "length_mins": 60,
          "price_cents": 2100,
          "price": "£21.00",
          "min_purchase": 10
        }
      ],
      "best_price": 2100,
      "best_one_hour_price": 2200,
      "languages": [],
      "qualifications": [
        "Drive iQ Pro"
      ],
      "affiliations": [
        "DSA Approved Driving Instructor",
        "Driving Instructors Association",
        "The Official Register of Driving Instructor Training",
        "Motor Schools Association"
      ],
      "specialities": [
        "Elderly Drivers",
        "Female Drivers",
        "Male Drivers",
        "Nervous Drivers",
        "Semi-experienced Drivers",
        "Young Drivers"
      ],
      "verified": false
    }
  }
}
```
This endpoint gets details of a instructor

### HTTP Request

`GET http://example.com/api/v1/instructors/:slug`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label



## Search intructors

> Sample request

```shell
curl -X GET "http://example.com/api/v1/instructors/search" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"auth_token": "some_token", "postcode": "MK5-8FT", car_type:"Manual", page: "1"}'
```

> Sample response

```json
{
  "success": 200,
  "data": [
    {
      "table": {
        "slug": "alan-melton1",
        "first_name": "Alan",
        "last_name": "Melton",
        "driving_school_name": "Atomdrivingschool@btinternet.com",
        "gearboxes": [
          "Manual"
        ],
        "gender": "M",
        "user_rating": 0,
        "testimonials_count": 0,
        "qualifications": [
          "Drive iQ Pro"
        ],
        "dsa_grade": "6",
        "location_name": "Leighton Buzzard, United Kingdom",
        "lat": 51.919684,
        "lon": -0.660657,
        "best_price": 2100,
        "best_one_hour_price": 2200,
        "description": "We are a no nonsense driving school and will have you on the road asap. Very flexible with times as we understand people lead a busy lifestyle these days. \r\nFirst lesson is £11 this is for you to see if your comfortable with the instructor and wish to carry on. \r\nAll services provided with pass plus motorway driving etc. \r\nCar is renewed every 18 months and is air conditioned.\r\nLessons can be as long or as short as you desire with prices to match length of the lesson you choose. \r\nText, email or simply phone to book your lesson now!",
        "avatar": {
          "url": "/assets/fallback/avatar/default-a3fa46ca7933dd2767c4b22d4c5034e9.jpg",
          "standard": {
            "url": "/assets/fallback/avatar/standard_default-3520b3d59ecb0207c53df02ff132805a.jpg"
          },
          "thumb": {
            "url": "/assets/fallback/avatar/thumb_default-c2e90a06644af95aa4c2e3f8a35d2490.jpg"
          }
        },
        "verified": false
      }
    },
    {
      "table": {
        "slug": "victor-fountain",
        "first_name": "Victor",
        "last_name": "Fountain",
        "driving_school_name": "AA Driving School",
        "gearboxes": [
          "Manual"
        ],
        "gender": "M",
        "user_rating": 0,
        "testimonials_count": 0,
        "qualifications": [
          "Drive iQ Pro",
          "RoSPA - Royal Society for the Prevention of Accidents"
        ],
        "dsa_grade": "4",
        "location_name": "Newport Pagnell, Buckinghamshire",
        "lat": 52.087462,
        "lon": -0.750777,
        "best_price": 2300,
        "best_one_hour_price": 2300,
        "description": "",
        "avatar": {
          "url": "/assets/fallback/avatar/default-a3fa46ca7933dd2767c4b22d4c5034e9.jpg",
          "standard": {
            "url": "/assets/fallback/avatar/standard_default-3520b3d59ecb0207c53df02ff132805a.jpg"
          },
          "thumb": {
            "url": "/assets/fallback/avatar/thumb_default-c2e90a06644af95aa4c2e3f8a35d2490.jpg"
          }
        },
        "verified": false
      }
    }
  ]
}
```
This endpoint searches instructors

### HTTP Request

`GET http://example.com/api/v1/instructors/search`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
auth_token | required | | auth_token received when signing in user
postcode | required | |
car_type | optional | | "Manual" or "Automatic"
page | optional | |
