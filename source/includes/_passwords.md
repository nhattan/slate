# Passwords

## Forgot password

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/password" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"email": "davidblack@gmail.com"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```

This endpoint creates a reset password token then send an email with reset password link to user

### HTTP Request

`POST http://example.com/api/v1/users/password`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
email | required | |


## Reset password

> Sample request

```shell
curl -X POST "http://example.com/api/v1/users/password/reset" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"reset_password_token": "some_token", "new_password": "some_password"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```

This endpoint resets user password

### HTTP Request

`POST http://example.com/api/v1/users/password/reset`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
reset_password_token | required | | get from [Forgot password](#forgot-password)
new_password | required | |
