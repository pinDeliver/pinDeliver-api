# Get order

Brödtext

### Endpoint
```
https://martinservera-test.pindeliver.com/api/v2_1/Order/get/{order_id}
```

### Authentication
```
Headers:
  X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX
  X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX
```

### Method
```
GET
```

### Example request
```C
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/order/get/{order_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example error response
```JSON
Error Response
[
  {
    "result": "error",
    "status": 404,
    "response": {
      "error_description": "No such order available"
    }
  }
]
```

### Example success response
```JSON
Success Response
{
    "order": {
        "id": "{order_id}",
        "name": "Scandinavium 1980-10-10",
        "order_type": "DELIVERY",
        "scheduled_date": "1980-10-10",
        "created_date": "1980-10-10 21:00:00",
        "delivery_group": "Smallwood DG",
        "status": "NOT_ROUTED",
        "num_customers": 0,
        "url": "https://cloud.pindeliver.com/api/v2_1/order/get/{order_id}"
    }
}
```
