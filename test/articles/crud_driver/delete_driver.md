# Delete driver

Used to delete a driver using the driver id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/driver/delete/{driver_id}
```

### Authentication
```
Headers:
  X-PINDELIVER-API-KEY:XXXX-XXXX-XXXX-XXXX
  X-PINDELIVER-API-CLIENT-KEY:XXXX-XXXX-XXXX-XXXX
```

### Method
```
POST
```

### Example request
```C
curl --location --request POST 'https://martinservera-test.pindeliver.com/api/v2_1/driver/delete/{driver_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data ''
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "Not Found"
    }
}
```

### Example success response
```JSON
{
    "result": "ok",
    "code": 200
}
```
