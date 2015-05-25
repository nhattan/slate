# Devices

## Register device

> Sample request

```shell
curl -X POST "http://example.com/api/v1/devices" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"token": "some_token", "platform": "android", "enabled": true}'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```
This endpoint registers a device used for push notification

### HTTP Request

`POST http://example.com/api/v1/devices`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
token | required | | Device token (aka registration id)
platform | required | | 'android' or 'ios'
enabled | optional | true | Enabled for receiving push notification



## Update device

> Sample request

```shell
curl -X POST "http://example.com/api/v1/devices/update" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -H 'Auth-Token: woofwoof' -d '{"token": "some_token", "platform": "ios", "enabled": false}'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```
This endpoint updates a device used for push notification

### HTTP Request

`POST http://example.com/api/v1/devices/update`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
token | optional | | Device token (aka registration id)
platform | optional | | 'android' or 'ios'
enabled | optional | | Enabled for receiving push notification



## Push notification

> Sample request

```shell
curl -X POST "http://example.com/api/v1/devices/notification" -H 'Content-Type: application/json' -H 'Api-Key: meowmeow' -d '{"platform": "android", "message": "Welcome to firstcar"}'
```

> Sample response

```json
{
  "success": 200,
  "data": {}
}
```
This endpoint sends a push notification to all devices in a specific platform

### HTTP Request

`POST http://example.com/api/v1/devices/notification`

### Query Parameters

Parameter | Required | Default | Description
--------- | ------- | ------- | -----------
wl | optional | firstcar | White label
platform | required | | 'android' or 'ios'
message | required | |
