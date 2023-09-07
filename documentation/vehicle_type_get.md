# Get vehicle type

Used to retrieve a vehicle type using the vehicle type id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/type/get/{vehicle_type_id}
```

### Authentication
```
Headers:
  X-PINDELIVER-API-KEY:XXXX-XXXX-XXXX-XXXX
  X-PINDELIVER-API-CLIENT-KEY:XXXX-XXXX-XXXX-XXXX
```

### Method
```
GET
```

### Example request
```C
curl --location 'https://cloud.pindeliver.com/api/v2_0/vehicle/type/get/{vehicle_type_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data ''
```

### Example data
```JSON

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
    "vehicle_type": {
        "id": "{vehicle_type_id}",
        "identifier": "pb",
        "name": "Personbil"
    }
}
```

---

# Get vehicle type by external id

Used to retrieve a vehicle type using the external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/type/get/extid/pb
```

### Authentication
```
Headers:
  X-PINDELIVER-API-KEY:XXXX-XXXX-XXXX-XXXX
  X-PINDELIVER-API-CLIENT-KEY:XXXX-XXXX-XXXX-XXXX
```

### Method
```
GET
```

### Example request
```C
curl --location 'https://cloud.pindeliver.com/api/v2_0/vehicle/type/get/extid/pb' \
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
        "error_description": "Can't find VehicleType with identifier: pbb"
    }
}
```

### Example success response
```JSON
{
    "vehicle_type": {
        "id": "{vehicle_type_id}",
        "identifier": "pb",
        "name": "Personbil"
    }
}
```

---

# Get all vehicle types

Used to retrieve all vehicle types

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/type/get/
```

### Authentication
```
Headers:
  X-PINDELIVER-API-KEY:XXXX-XXXX-XXXX-XXXX
  X-PINDELIVER-API-CLIENT-KEY:XXXX-XXXX-XXXX-XXXX
```

### Method
```
GET
```

### Example request
```C
curl --location 'https://martinservera-test.pindeliver.com/api/v2_0/vehicle/type/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data ''
```

### Example success response
```JSON
{
    "vehicle_types": [
        {
            "id": "{vehicle_type_id}",
            "identifier": "pb",
            "name": "Personbil"
        }
    ]
}
```
