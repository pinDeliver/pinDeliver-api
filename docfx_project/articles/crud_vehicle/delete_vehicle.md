# Delete vehicle

Used to delete a vehicle using the vehicle id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/vehicle/delete/{vehicle_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/vehicle/delete/{vehicle_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "No such vehicle"
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
