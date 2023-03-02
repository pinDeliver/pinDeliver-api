# Add driver

Connected to a [delivery group](delivery_group_add.md). Make sure you've created a delivery group before creating a driver. A driver is not needed before [adding a route](route_add.md) but it is necessary to create one to be able to start the route later on. The driver can also be connected to a [vehicle](vehicle_add.md).

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/driver/add
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
curl --location 'https://martinservera-test.pindeliver.com/api/v2_1/driver/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "driver": {
        "name": "Anders Andersson",
        "phone": "0700000000",
        "email": "email@email.com",
        "language_code": "sv_SE",
        "premium_scanning": false,
        "delivery_groups": [
            {
                "id": {delivery_group_id}
            },
            {
                "id": {delivery_group_id}
            }
        ],
        "carrier": {
        "id": {carrier_id}
        }
    }
}'
```

### Example data
```JSON
{
    "driver": {
        "name": "Anders Andersson",
        "phone": "0700000000",
        "email": "email@email.com",
        "language_code": "sv_SE",
        "premium_scanning": false,
        "delivery_groups": [
            {
                "id": "{delivery_group_id}"
            },
            {
                "id": "{delivery_group_id}"
            }
        ],
        "carrier": {
        "id": "{carrier_id}"
        }
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
    "result": "ok",
    "code": 200,
    "data": "{driver_id}",
    "url": "http://martinservera-test.pindeliver.com/api/v2_1/driver/get/{driver_id}"
}
```

---

# Input format

### Driver object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|name|string|The name of the driver|Anders Andersson|
|phone|string or null|The drivers phone number|0701234567|
|email|string or null|The drivers email|anders@email.com|
|language_code|string or null|The preferred language used by the driver. en_GB, sv_SE|sv_SE|
|premium_scanning|boolean or null|Shows if the driver is using premium scanning or not|false|
|delivery_groups|||Details below|
|carrier|||Details below|

### Delivery group object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|id|number or null|The id of the delivery group(s) connected to the driver|10, 11|

### Carrier object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|id|number or null|The id of the carrier connected to the driver|20|
