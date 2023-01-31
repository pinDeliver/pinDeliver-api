# Get vehicle

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/vehicle/get/{vehicle_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/vehicle/get/{vehicle_id}' \
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
        "name": "Ed force one",
        "number_of_resources": 1,
        "delivery_group": "Smallwood DG",
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
        "url": "https://cloud.pindeliver.com/api/v2_1/vehicle/get/{vehicle_id}"
    }
}
```

---

# Get all vehicles

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/vehicle/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/vehicle/get' \
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
            "name": "Ed force one",
            "number_of_resources": 1,
            "delivery_group": "Smallwood DG",
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
            "url": "https://cloud.pindeliver.com/api/v2_1/vehicle/get/{vehicle_id}"
        }
    ]
}
```

---

# Output format

**Vehicle Object Properties**

|Field              |Explanation      |Description          |Example      |
|-------------------|-----------------|---------------------|-------------|
|id                 |integer          |Id of this vehicle   |1510         |
|name               |string           |Name of this vehicle |My Van       |
|number_of_resources|integer          |Maximal number of instances of this vehicle to be used in an optimization|5|
|external_resource_id|string|External identifier for the resource|X-COMPANY-RESOURCE-ID|
|delivery_group|string|The name of the delivery group that the vehicle belongs to|My Delivery Group|
|timewindow_start|string on the format HH:mm|The earliest time that the vehicle may start its route|08:00|
|timewindow_end|string on the format HH:mm|The latest time that the vehicle must have finished its route|21:00|
|fixed_start_time|boolean|Indicates whether the vehicle should start at its timewindow_start|true or false|
|start_location_address|string|The address where the vehicle starts its route|Kungsgatan 3, Stockholm, Sverige|
|start_location_latitude|number|The latitude where the vehicle starts its route|Kungsgatan 3, Stockholm, Sverige|
|start_location_longitude|number|The longitude where the vehicle starts its route|Kungsgatan 3, Stockholm, Sverige|
|end_location_address|string|The address where the vehicle ends its route|Kungsgatan 3, Stockholm, Sverige|
|end_location_latitude|number|The latitude where the vehicle ends its route|Kungsgatan 3, Stockholm, Sverige|
|end_location_longitude|number|The longitude where the vehicle ends its route|Kungsgatan 3, Stockholm, Sverige|
|max_weight|integer|The maximum weight that the vehicle may carry|400|
|max_volume|integer|The maximum volume that the vehicle may carry|150|
|co_2|integer|The co2 footprint of the vehicle|44|
|tags|string|A semicolon separated list of vehicle tags|tag1;tag2|
|loading_zone|string|Which loading zone the goods is located	Loading zone|A|
|default_driver_id	|integer|ID of an existing driver|1337|
|default_driver_name|string|Name of the default driver|Driver Name|
|default_driver_contact_type|string|SMS or EMAIL the preferred way of contacting the driver.|SMS|
|default_driver_phone|string|Default driver cellphone number|0701-12 34 56|
|default_driver_email|string|Default driver email address|name@example.com|
|url|string|The URL for retrieving the individual vehicle in this API|
