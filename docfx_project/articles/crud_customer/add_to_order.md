# Add to order

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/order/addCustomer/{order_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/addCustomer/{order_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
        "customers": [
        {
            "id": {customer_id},
            "name": "Steve Harris",
            "postal_address": "Andra Långgatan 17",
            "city": "Göteborg",
            "service": {
            }
        }
    ]
}'
```

### Example data
```JSON
{
        "customers": [
        {
            "id": "{customer_id}",
            "name": "Steve Harris",
            "postal_address": "Andra Långgatan 17",
            "city": "Göteborg",
            "service": {
            }
        }
    ]
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such order available"
}
```

### Example success response
```JSON
[
    {
        "result": "ok",
        "data": "{customer_id}",
        "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}"
    }
]
```
