# Add customer

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/add
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "customer": {
        "order_id":{order_id},
        "route_id":{route_id},
        "position_in_route":1,
        "name":"Steve Harris",
        "postal_address":"Andra Långgatan 7",
        "city":"Göteborg",
        "service": {
        }
    }
}'
```

### Simple example data
```JSON
{
    "customer": {
        "order_id":"{order_id}",
        "route_id":"{route_id}",
        "position_in_route":1,
        "name":"Steve Harris",
        "postal_address":"Andra Långgatan 7",
        "city":"Göteborg",
        "service": {
        }
    }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "customer": {
        "order_id":{order_id},
        "route_id":{route_id},
        "delivery_group": "Smallwood DG",
        "name": "Steve Harris",
        "language_code": "sv_SE",
        "postal_address": "Andra Långgatan 7",
        "zipcode": "41303",
        "city": "Göteborg",
        "country_code": "sv",
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
            "tracking_url": "https://my.pindeliver.com/8ottrbilqbt"
        },
        "customer_type": "b2c"
    }
}'
```

### Advanced example data
```JSON
{
    "customer": {
        "order_id":"{order_id}",
        "route_id":"{route_id}",
        "delivery_group": "Smallwood DG",
        "name": "Steve Harris",
        "language_code": "sv_SE",
        "postal_address": "Andra Långgatan 7",
        "zipcode": "41303",
        "city": "Göteborg",
        "country_code": "sv",
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
            "tracking_url": "https://my.pindeliver.com/8ottrbilqbt"
        },
        "customer_type": "b2c"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "data": "add_customer2 could not be validated: [customer.service] The property service is required"
}
```

### Example success response
```JSON
{
    "result": "ok",
    "status": 200,
    "data": "{customer_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}"
}
```
