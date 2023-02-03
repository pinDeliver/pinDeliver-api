# Update route

Used to update a route using the route id

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

|Property             |Type     |Description          |Example      |Default  |   
|---------------------|---------|---------------------|-------------|---------|
|name|string or null|Name of this route|Scandinavium|
|predefined_route_name|string or null|Name for the predefined routes that is created through the haulage portal|4TGG5|
|scheduled|string or null|The date a route is scheduled to start|1980-10-10T10:00:00.234+02:00|
|vehicle|||Details below|

### Vehicle Object Properties

|Property              |Type      |Description          |Example      |Default  |    
|-------------------|-----------------|---------------------|-------------|---------|
|name<font color='red'>*</font>              |string           |Name of this vehicle |My Van       |         |
|number_of_resources|integer|Maximal number of instances of this vehicle to be used in an optimization|5|1|
|external_resource_id|string|External identifier for the resource|X-COMPANY-RESOURCE-ID|null|
|delivery_group<font color='red'>*</font>|string|The name of the delivery group that the vehicle belongs to|My Delivery Group|
|timewindow_start<font color='red'>*</font>|string on the format HH:mm|The earliest time that the vehicle may start its route|08:00|
|timewindow_end<font color='red'>*</font>|string on the format HH:mm|The latest time that the vehicle must have finished it's route|21:00|
|fixed_start_time|boolean|Indicates whether the vehicle should start at its timewindow_start|true or false|false|
|start_location_address<font color='red'>*</font>|string|The address where the vehicle starts its route|Kungsgatan 3, Stockholm, Sverige|
|start_location_latitude|number|The latitude where the vehicle starts its route. If not specified then a geocoding lookup based on start_location_address is made.|Kungsgatan 3, Stockholm, Sverige|
|start_location_longitude|number|The longitude where the vehicle starts its route. If not specified then a geocoding lookup based on start_location_address is made.|Kungsgatan 3, Stockholm, Sverige|
|end_location_address<font color='red'>*</font>|string|The address where the vehicle ends its route|Kungsgatan 3, Stockholm, Sverige|
|end_location_latitude|number|The latitude where the vehicle ends its route. If not specified then a geocoding lookup based on start_location_address is made.|Kungsgatan 3, Stockholm, Sverige|
|end_location_longitude|number|The longitude where the vehicle ends its route. If not specified then a geocoding lookup based on start_location_address is made.|Kungsgatan 3, Stockholm, Sverige|
|max_weight|integer|The maximum weight that the vehicle may carry|400|0|
|max_volume|integer|The maximum volume that the vehicle may carry|150|0|
|co_2|integer|The co2 footprint of the vehicle|44|null|
|tags|string|A semicolon separated list of vehicle tags|tag1;tag2|
|loading_zone|string|Which loading zone the goods is located|Loading zone A|
|default_driver_id|integer|ID of an existing driver, if default_driver_id is provided, default_driver_name, default_driver_phone & default_driver_email will be ignored.|1337|null|
|default_driver_name|string|Name of a default driver who doesn't exist, if default_driver_name is provided system will create a new driver with the given name at least default_driver_phone or default_driver_email is required to create a driver|Driver Name|null|
|default_driver_contact_type|string|SMS or EMAIL the preferred way of contacting the driver.|SMS|
|default_driver_phone|string|Cellphone number of a default driver who doesn't exist, used for assigning a route to driver via cellphone number.|0701-12 34 56|null|
|default_driver_email|string|Email address of a default driver who doesn't exist, used for assigning a route to driver via email.|name@example.com|null|
|max_working_time|integer or null|The max time a driver can work in go|8|
|min_working_time|integer or null|The minimum time a driver can work|5|
|max_working_time_without_break|integer or null|The maximum time a drvier can work before neeeding a break|4|
|max_distance|number or null|The max distance the driver can go. In kilometers|100|
|break_duration|integer or null|The duration of a break|15|
|speed_factor|integer or null|The speed in which the vehicle can drive. If it's a busy time, the speed is probably lower. Ranging from 0,5 to 2|0,8|
|carrier|string or null|The name of the carrier|TGG|
|carrier_id|integer or null|The id of the carrier|12345|
