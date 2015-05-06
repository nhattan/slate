# Users

## Get a user


```shell
curl "http://example.com/api/v1/users"
  -H 'Content-Type: application/json'
  -H 'Api-Key: meowmeowmeow'
  -d '{"auth_token": "some_token"}'
```

> The above command returns JSON structured like this:

```json
{
  "data": {
      "user": {
          "id": 3,
          "email": "nhattan14@gmail.com",
          "created_at": "2015-04-21T03:28:46.000Z",
          "updated_at": "2015-04-21T08:58:39.636Z",
          "accept_terms": true,
          "opt_in_retention": true,
          "opt_in_acquisition": true,
          "title": "Mr",
          "first_name": "Tan6",
          "last_name": "Nguyen",
          "phone_1": null,
          "phone_2": null,
          "white_label_id": 1,
          "authentication_token": "32_LpcrRZh6cjiFysR8U",
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

This endpoint retrieves a user.

### HTTP Request

`GET http://example.com/api/v1/users`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not pass it will automatically set to current white label
auth_token | required | | auth_token received when signin user

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>
