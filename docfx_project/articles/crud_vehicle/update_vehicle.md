# Update vehicle

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/vehicle/update/{vehicle_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/vehicle/update/{vehicle_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "vehicle": {
        "name": "Ed force two",
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "timewindow_end": "18:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_address": "Ullevigatan, Göteborg, Sverige"
    }
}'
```

### Example data
```JSON
{
    "vehicle": {
        "name": "Ed force two",
        "delivery_group": "Smallwood DG",
        "timewindow_start": "08:30",
        "timewindow_end": "18:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_address": "Ullevigatan, Göteborg, Sverige"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "update_vehicle2 could not be validated: [vehicle.delivery_group] The property delivery_group is required"
    }
}
```

### Example success response
```JSON
{
    "vehicle": "Ed force two",
    "result": "ok",
    "code": 200,
    "data": "{vehicle_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}"
}
```
