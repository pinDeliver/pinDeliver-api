# Add vehicle type

Connected to a [vehicle](/articles/crud_vehicle/add_vehicle.html). Make sure you've created a vehicle before creating a vehicle type.

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/vehicle/type/add
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
curl --location 'https://martinservera-test.pindeliver.com/api/v2_1/vehicle/type/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data '{
    "vehicle_type": {
        "identifier": "pb",
        "name": "Personbil"
    }
}'
```

### Example data
```JSON
{
    "vehicle_type": {
        "identifier": "pb",
        "name": "Personbil"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "add_vehicle_type2 could not be validated: [vehicle_type.name] The property name is required"
    }
}
```

### Example success response
```JSON
{
    "vehicle_type": "pb",
    "result": "ok",
    "code": 200,
    "data": "{vehicle_type_id}",
    "url": "http://martinservera-test.pindeliver.com/api/v2_0/vehicle/type/get/{vehicle_type_id}"
}
```

---

# Input format

### Vehicle type object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|name|string|The name of the vehicle type|Personbil|
|identifier|string|The identifier of the vehicle type|pb|
