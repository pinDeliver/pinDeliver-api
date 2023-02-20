# Get customer

Used to retrieve a customer using the customer id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such customer available"
    }
]
```

### Example success response
```JSON
{
    "customer": {
        "id": "{customer_id}",
        "order_id": "{order_id}",
        "delivery_group": "DeliveryGroup",
        "name": "Anders Andersson",
        "language_code": "sv_SE",
        "postal_address": "Andra Långgatan 7",
        "zipcode": "41303",
        "city": "Göteborg",
        "country_code": "",
        "phone_cell": "0700000000",
        "position_lat": 57.699432,
        "position_lng": 11.950743,
        "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}",
        "service": {
            "type": "dropoff",
            "sms_sender": "Ovning",
            "sender_name": "pinDeliver",
            "recycling": [],
            "packages": [],
            "tracking_number": "123456789",
            "vehicle_tags": "Tag1",
            "timewindow_start": "01:01",
            "timewindow_end": "23:15",
            "requested_delivery_date": "2023-01-23",
            "priority": "normal",
            "tracking_url": "https://my.pindeliver.com/8ottvq5s0v5"
        },
        "customer_type": "b2c"
    }
}
```

---

# Get customer using external id

Used to retrieve a customer using the customer external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/get/extid/{external_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/customer/get/extid/{external_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such customer available"
    }
]
```

### Example success response
```JSON
{
    "customer": {
        "id": "{customer_id}",
        "order_id": "{order_id}",
        "delivery_group": "DeliveryGroup",
        "name": "Anders Andersson",
        "language_code": "sv_SE",
        "postal_address": "Andra Långgatan 7",
        "zipcode": "41303",
        "city": "Göteborg",
        "country_code": "",
        "phone_cell": "0700000000",
        "position_lat": 57.699432,
        "position_lng": 11.950743,
        "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}",
        "service": {
            "type": "dropoff",
            "sms_sender": "Ovning",
            "sender_name": "pinDeliver",
            "recycling": [],
            "packages": [],
            "tracking_number": "123456789",
            "vehicle_tags": "Tag1",
            "timewindow_start": "01:01",
            "timewindow_end": "23:15",
            "requested_delivery_date": "2023-01-23",
            "priority": "normal",
            "tracking_url": "https://my.pindeliver.com/8ottvq5s0v5"
        },
        "customer_type": "b2c"
    }
}
```

---

# Query parameters

### Endpoint example
```
https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}?all
```

If you want to use multiple parameters at the same time you can add them after the first parameter using "&".
For example: ?all&order&routes.

### Parameters

|Property|Description|
|--------|-----------|
|?all|Get all info for the specific customer|
|?order|Get orders for the specific customer|
|?routes|Get routes for the specific customer|
|?stops|Get stops for the specific customer|
|?shipping_labels|Get shipping labels for the specific customer|
|?messages|Get messages for the specific customer|
