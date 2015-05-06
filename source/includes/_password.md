# Passwords

## Forgot password

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/passwords" -H 'Content-Type: application/json' -H 'Api-Key: meowmeowmeow' -d '{"email": "nhattan@gmail.com"}'
```

> Sample response

```json
{
  "data": {}
}
```

This endpoint create a reset password token then send an email with reset password link to user

### HTTP Request

`POST http://example.com/api/v1/users/passwords`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | | If wl is not passed it will automatically set to current white label
email | required | |
