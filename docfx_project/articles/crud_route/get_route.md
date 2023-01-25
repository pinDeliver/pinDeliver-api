# Get route

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/get/{route_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/route/get/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example data
```JSON

```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 405,
        "data": "Method not allowed"
    }
]
```

### Example success response
```JSON
{
    "route": {
        "id": "{route_id}",
        "order_id": "{order_id}",
        "name": "E1",
        "linehaul": false,
        "scheduled_start_time": "1980-10-10 10:00:00",
        "distance": 0,
        "total_drive_time": 0,
        "total_idle_time": 0,
        "speed_factor": 1,
        "num_customers": 0,
        "locked": false,
        "optimized": false,
        "changed": false,
        "assigned": false,
        "loading_started": false,
        "loading_completed": false,
        "quality_check_completed": false,
        "latest_lat": 0,
        "latest_lng": 0,
        "vehicle": {
            "name": "Ed force one",
            "timewindow_start": "00:00",
            "timewindow_end": "23:59",
            "start_lat": 57.6995883,
            "start_lng": 11.9529051,
            "end_lat": 57.6973714,
            "end_lng": 11.979319,
            "start_position_name": "Järntorget, Göteborg, Sverige",
            "end_position_name": "Götaplatsen, Göteborg, Sverige",
            "max_weight": 0,
            "max_volume": 0,
            "max_volume_2": 0,
            "fixed_start_time": false
        },
        "url": "https://cloud.pindeliver.com/api/v2_1/route/get/{route_id}"
    }
}
```

# Get all routes

Brödtext

### Endpoint
```
https:/cloud.pindeliver.com/api/v2_1/Route/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/Route/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example success response
```JSON
{
    "routes": [
        {
            "id": "{route_id}",
            "order_id": "{order_id}",
            "name": "Ed force one",
            "linehaul": false,
            "scheduled_start_time": "1980-10-10 06:50:37",
            "scheduled_end_time": "1980-10-10 07:28:17",
            "duration": 2260,
            "distance": 17418,
            "total_drive_time": 1180,
            "total_idle_time": 0,
            "speed_factor": 1,
            "stop_time": 5,
            "num_customers": 2,
            "locked": false,
            "optimized": true,
            "changed": false,
            "assigned": false,
            "loading_started": false,
            "loading_completed": false,
            "quality_check_completed": false,
            "latest_lat": 0,
            "latest_lng": 0,
            "vehicle": {
                "id": 1013,
                "name": "Ed force one",
                "timewindow_start": "06:00",
                "timewindow_end": "18:00",
                "start_lat": 57.71066339999999,
                "start_lng": 11.969655800000055,
                "end_lat": 57.71066339999999,
                "end_lng": 11.969655800000055,
                "start_position_name": "Nils Ericsonsplatsen, Göteborg, Sverige",
                "end_position_name": "Nils Ericsonsplatsen, Göteborg, Sverige",
                "max_weight": 1500,
                "fixed_start_time": false
            },
            "url": "https://cloud.pindeliver.com/api/v2_1/route/get/{route_id}"
        }
    ],
    "exec_time": 0.053381919860839844
}
```
