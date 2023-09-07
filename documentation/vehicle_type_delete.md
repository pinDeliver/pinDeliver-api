# Delete vehicle type

Used to delete a vehicle type using the vehicle type id.

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/type/delete/{vehicle_type_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/vehicle/type/delete/{vehicle_type_id}' \
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
        "error_description": "Can't find VehicleType with id: {vehicle_type_id}"
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
