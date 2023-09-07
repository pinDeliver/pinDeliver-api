# Get route

Used to retrieve a route using the route id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/route/get/{route_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/route/get/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
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
        "name": "Scandinavium 1980-10-10",
        "linehaul": false,
        "vehicle_name": "Vehicle1",
        "vehicle_timewindow_start": "06:00",
        "vehicle_timewindow_end": "18:00",
        "locked": false,
        "assigned": false,
        "changed": true,
        "driver_name": "",
        "driver_phone": "",
        "scheduled_start_time": "2023-09-07 06:20:17",
        "scheduled_end_time": "2023-09-07 09:33:25",
        "duration": 11588,
        "total_drive_time": 6908,
        "total_idle_time": 0,
        "distance": 128863,
        "start_lat": 57.71066339999999,
        "start_lng": 11.969655800000055,
        "end_lat": 57.71066339999999,
        "end_lng": 11.969655800000055,
        "start_position_name": "Nils Ericsonsplatsen, Göteborg, Sverige",
        "end_position_name": "Nils Ericsonsplatsen, Göteborg, Sverige",
        "speed_factor": 1,
        "stop_time": 5,
        "num_customers": 6,
        "loading_started": false,
        "loading_completed": false,
        "quality_check_completed": false,
        "url": "https://cloud.pindeliver.com/api/v2_0/route/get/route_id"
    }
}
```

---

# Query parameters

### Endpoint example
```
https://cloud.pindeliver.com/api/v2_0/route/get/{route_id}?all
```

If you want to use multiple parameters at the same time you can add them after the first parameter using "&".
For example: ?all&order&routes.

### Parameters

|Property|Description|
|--------|-----------|
|?all|Get all info for the specific route|
|?order|Get orders for the specific route|
|?routes|Get routes for the specific route|
|?stops|Get stops for the specific route|
|?customer|Get customers for the specific route|
