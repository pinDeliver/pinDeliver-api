# Delete a carrier

Used to delete a carrier using the carrier id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/carrier/delete/{carrier_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/carrier/delete/{carrier_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "can't find carrier on server {carrier_id}"
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
