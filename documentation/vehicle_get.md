# Get vehicle

Used to retrieve a vehicle using the vehicle id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}' \
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
        "error_description": "No such vehicle"
    }
}
```

### Example success response
```JSON
{
    "vehicle": {
        "id": "{vehicle_id}",
        "name": "Vehicle1",
        "number_of_resources": 1,
        "delivery_group": "DeliveryGroup",
        "timewindow_start": "08:30",
        "timewindow_end": "18:30",
        "break_duration": 0,
        "fixed_start_time": false,
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "start_location_latitude": 57.70887,
        "start_location_longitude": 11.97456,
        "end_location_address": "Ullevigatan 5, Göteborg, Sverige",
        "end_location_latitude": 57.707119,
        "end_location_longitude": 11.9869172,
        "loading_zone": "1975",
        "url": "https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}"
    }
}
```

---

# Get all vehicles

Used to retrieve all vehicles

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/vehicle/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example success response
```JSON
{
    "vehicles": [
        {
            "id": "{vehicle_id}",
            "name": "Vehicle1",
            "number_of_resources": 1,
            "delivery_group": "DeliveryGroup",
            "timewindow_start": "08:30",
            "timewindow_end": "18:30",
            "break_duration": 0,
            "fixed_start_time": false,
            "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
            "start_location_latitude": 57.70887,
            "start_location_longitude": 11.97456,
            "end_location_address": "Ullevigatan 5, Göteborg, Sverige",
            "end_location_latitude": 57.707119,
            "end_location_longitude": 11.9869172,
            "loading_zone": "1975",
            "url": "https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}"
        }
    ]
}
```
