# Add route

Connected to an [order](/articles/crud_order/add_order.html) and a [vehicle](/articles/crud_vehicle/add_vehicle.html). Make sure you've created an order and a vehicle before creating a route

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/add
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/route/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "route": {
        "order_id": {route_id},
        "name": "E1",
        "scheduled": "1980-10-10T10:00:00.234+02:00",
        "vehicle": {
            "name": "Ed force one",
            "delivery_group": "Smallwood DG",
            "start_location_address": "Järntorget, Göteborg, Sverige",
            "timewindow_start": "00:00",
            "timewindow_end": "23:59"
        }
    }
}'
```

### Simple example data
```JSON
{
    "route": {
        "order_id": "{route_id}",
        "name": "E1",
        "scheduled": "1980-10-10T10:00:00.234+02:00",
        "vehicle": {
            "name": "Ed force one",
            "delivery_group": "Smallwood DG",
            "start_location_address": "Järntorget, Göteborg, Sverige",
            "timewindow_start": "00:00",
            "timewindow_end": "23:59"
        }
    }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/route/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "route": {
        "order_id": "{order_id}",
        "name": "E1",
        "linehaul": false,
        "scheduled": "1980-10-10T10:00:00.234+02:00",
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
            "delivery_group": "Smallwood DG",
            "start_location_address": "Järntorget, Göteborg, Sverige",
            "timewindow_start": "00:00",
            "timewindow_end": "23:59",
            "start_lat": 57.6995883,
            "start_lng": 11.9529051,
            "start_position_name": "Järntorget, Göteborg, Sverige",
            "end_position_name": "Järntorget, Göteborg, Sverige",
            "end_lat": 57.6995883,
            "end_lng": 11.9529051,
            "max_weight": 0,
            "max_volume": 0,
            "max_volume_2": 0,
            "fixed_start_time": false
        }
    }
}'
```

### Advanced example data
```JSON
{
    "route": {
        "order_id": "{order_id}",
        "name": "E1",
        "linehaul": false,
        "scheduled": "1980-10-10T10:00:00.234+02:00",
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
            "delivery_group": "Smallwood DG",
            "start_location_address": "Järntorget, Göteborg, Sverige",
            "timewindow_start": "00:00",
            "timewindow_end": "23:59",
            "start_lat": 57.6995883,
            "start_lng": 11.9529051,
            "start_position_name": "Järntorget, Göteborg, Sverige",
            "end_position_name": "Järntorget, Göteborg, Sverige",
            "end_lat": 57.6995883,
            "end_lng": 11.9529051,
            "max_weight": 0,
            "max_volume": 0,
            "max_volume_2": 0,
            "fixed_start_time": false
        }
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "data": "add_route2 could not be validated: [route.order_id] The property order_id is required"
}
```

### Example success response
```JSON
{
    "route": "E1",
    "result": "ok",
    "status": 200,
    "data": "{route_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/Route/get/{route_id}"
}
```

---

# Output format

### Route Object Properties

Fields marked with <font color='red'>*</font> are required

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|order_id<font color='red'>*</font>|integer|Id of the order that the route is added on to|12345|
|name<font color='red'>*</font>|string|Name of this route|Scandinavium|
|predefined_route_name|string or null|Name for the predefined routes that is created through the haulage portal|4TGG5|
|scheduled<font color='red'>*</font>|string|The date a route is scheduled to start|1980-10-10T10:00:00.234+02:00|
|vehicle<font color='red'>*</font>|||Details in [add vehicle](/articles/crud_vehicle/add_vehicle.html) under output format|
