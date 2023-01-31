# Update route

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/update/{route_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/Route/update/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "route": [
        {
            "scheduled_start_time": "2023-01-25 21:00:00",
            "scheduled_end_time": "2023-01-25 23:47:21"
        }
    ]
}'
```

### Example data
```JSON
{
    "route": {
            "scheduled_start_time": "2023-01-25 21:00:00",
            "scheduled_end_time": "2023-01-25 23:47:21"
        }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such route available",
    "exec_time": 0.034607887268066406
}
```

### Example success response
```JSON
{
    "route": "Ed force one",
    "result": "ok",
    "status": 200,
    "data": "{route_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/Route/get/{route_id}",
    "exec_time": 0.05251193046569824
}
```

---

# Output format

### Route Object Properties

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|name|string or null|||
|predefined_route_name|string or null|||
|scheduled|string or null|||
|vehicle|||Details below|

### Vehicle Object Properties

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|name|string or null|||
|number_of_resources|integer or null|||
|external_resource_id|string or null|||
|delivery_group|string or null|||
|timewindow_start|string or null|||
|timewindow_end|string or null|||
|fixed_start_time|boolean or null|||
|start_location_address|string or null|||
|start_location_latitude|number or null|||
|start_location_longitude|number or null|||
|end_location_address|string or null|||
|end_location_latitude|number or null|||
|end_location_longitude|number or null|||
|max_weight|integer or null|||
|max_volume|integer or null|||
|max_volume_2|integer or null|||
|co_2|integer or null|||
|tags|string or null|||
|loading_zone|string or null|||
|default_driver_id|string or null|||
|default_driver_name|string or null|||
|default_driver_phone|string or null|||
|default_driver_contact_type|string or null|||
|default_driver_email|string or null|||
|max_working_time|integer or null|||
|min_working_time|integer or null|||
|max_working_time_without_break|integer or null|||
|max_distance|number or null|||
|break_duration|integer or null|||
|speed_factor|integer or null||1,5|
|carrier|string or null|||
|carrier_id|integer or null|||
