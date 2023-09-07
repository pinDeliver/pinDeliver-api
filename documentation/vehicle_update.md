# Update vehicle

Used to update a vehicle using the vehicle id

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
        "name": "Vehicle2",
        "delivery_group": "DeliveryGroup",
        "timewindow_start": "08:30",
        "timewindow_end": "18:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_address": "Ullevigatan 5, Göteborg, Sverige"
    }
}'
```

### Example data
```JSON
{
    "vehicle": {
        "name": "Vehicle2",
        "delivery_group": "DeliveryGroup",
        "timewindow_start": "08:30",
        "timewindow_end": "18:30",
        "start_location_address": "Valhallavägen 1, Göteborg, Sverige",
        "end_location_address": "Ullevigatan 5, Göteborg, Sverige"
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
    "vehicle": "Vehicle2",
    "result": "ok",
    "code": 200,
    "data": "{vehicle_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/vehicle/get/{vehicle_id}"
}
```

---

# Output format

### Vehicle Object Properties

  Fields marked with <font color='red'>*</font> are required

|Property              |Type     |Description          |Example      |Default  |    
|-------------------|-----------------|---------------------|-------------|---------|
|name<font color='red'>*</font>             |string           |Name of this vehicle |My Van       |         |
|number_of_resources|integer|Maximal number of instances of this vehicle to be used in an optimization|5|1|
|external_resource_id|string|External identifier for the resource|X-COMPANY-RESOURCE-ID|NULL|
|delivery_group<font color='red'>*</font>|string|The name of the delivery group that the vehicle belongs to|My Delivery Group|
|timewindow_start<font color='red'>*</font>|string on the format HH:mm|The earliest time that the vehicle may start its route|08:00|
|timewindow_end<font color='red'>*</font>|string on the format HH:mm|The latest time that the vehicle must have finished its route|21:00|
|fixed_start_time|boolean|Indicates whether the vehicle should start at its timewindow_start|true or false	false|
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
|default_driver_id|integer|ID of an existing driver, if default_driver_id is provided, default_driver_name, default_driver_phone & default_driver_email will be ignored.|1337|NULL|
|default_driver_name|string|Name of a default driver who doesn't exist, if default_driver_name is provided system will create a new driver with the given name at least default_driver_phone or default_driver_email is required to create a driver|Driver Name|NULL|
|default_driver_contact_type|string|SMS or EMAIL the preferred way of contacting the driver.|SMS|
|default_driver_phone|string|Cellphone number of a default driver who doesn't exist, used for assigning a route to driver via cellphone number.|0701-12 34 56|NULL|
|default_driver_email|string|Email address of a default driver who doesn't exist, used for assigning a route to driver via email.|name@example.com|NULL|
