# Update delivery group

Used to update a delivery group using the delivery group id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/delivery_group/update/{delivery_group_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/delivery_group/update/{delivery_group_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "delivery_group": {

       "name": "DeliveryGroup"
    }
}'
```

### Example data
```JSON
{
    "delivery_group": {

        "name": "DeliveryGroup"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "Request must contain valid json"
    }
}
```

### Example success response
```JSON
{
    "delivery_group": "DeliveryGroup",
    "result": "ok",
    "code": 200,
    "data": "{delivery_group_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/delivery_group/get/{delivery_group_id}"
}
```

---

# Input format

---

# Input format

### Delivery Group object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|name<font color='red'>*</font>|string|Name of this delivery group.|Göteborg|
|identifier<font color='red'>*</font>|string or null|Unique identifier of this delivery group. <br><font color='red'>If identifier is null the identifier will be set to this delivery group name.</font>|Göteborg|
|base_stop_time|integer|Base stop time of this delivery group to be used in an optimization.|5|
apartment_stop_time|integer|"base_stop_time" + "apartment_stop_time" equals the total stop time for customer who live in apartments, used in an optimization.|2|
depot_reload_time_minutes|integer|Number of minutes it takes to reload a vehicle at a depot stop, used in an optimization.|65|
depot_address|string|The address where the depot is located.|Nils Ericsonsplatsen 3, 411 03 Göteborg|
depot_location_latitude|number|The latitude where the depot is located.|57.7091409|
depot_location_longitude|number|The longitude where the depot is located.|11.9712367|
