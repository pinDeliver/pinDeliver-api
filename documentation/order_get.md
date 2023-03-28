# Get order

Used to retrieve an order using the order id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/Order/get/{order_id}
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
        "delivery_group": "DeliveryGroup",
        "status": "NOT_ROUTED",
        "num_customers": 0,
        "url": "https://cloud.pindeliver.com/api/v2_1/order/get/{order_id}"
    }
}
```

---

# Query parameters

### Endpoint example
```
https://cloud.pindeliver.com/api/v2_1/order/get/{order_id}?all
```

If you want to use multiple parameters at the same time you can add them after the first parameter using "&".
For example: ?all&order&routes.

### Parameters

|Property|Description|
|--------|-----------|
|?all|Get all info for the specific order|
|?routes|Get routes for the specific order|
|?stops|Get stops for the specific order|
|?customer|Get customers for the specific order|
