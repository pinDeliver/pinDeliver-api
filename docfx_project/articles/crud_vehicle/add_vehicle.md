# Add vehicle

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/add
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

### Simple example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/vehicle/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "vehicle": {
        "name": "Ed force one",
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige"
    }
}'
```

### Simple example data
```JSON
{
    "vehicle": {
        "name": "Ed force one",
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige"
    }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/vehicle/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "vehicle": {
        "name": "Ed force one",
        "number_of_resources": 1,
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "timewindow_end": "23:45",
        "break_duration": 5,
        "fixed_start_time": false,
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "start_location_latitude": 57.70887,
        "start_location_longitude": 11.97456,
        "end_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_latitude": 57.70887,
        "end_location_longitude": 11.97456
    }
}'
```

### Advanced example data
```JSON
{
    "vehicle": {
        "name": "Ed force one",
        "number_of_resources": 1,
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "timewindow_end": "23:45",
        "break_duration": 5,
        "fixed_start_time": false,
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "start_location_latitude": 57.70887,
        "start_location_longitude": 11.97456,
        "end_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_latitude": 57.70887,
        "end_location_longitude": 11.97456
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "add_vehicle2 could not be validated: [vehicle.name] The property name is required"
    }
}
```

### Example success response
```JSON
{
    "vehicle": "Ed force one",
    "result": "ok",
    "code": 200,
    "data": "{vehicle_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}"
}
```
