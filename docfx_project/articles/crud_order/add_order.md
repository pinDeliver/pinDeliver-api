# Add order

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/order/add
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "order":{
            "name":"Scandinavium 1980-10-10",
            "delivery_group":"Smallwood DG",
            "order_type":"delivery",
            "scheduled_date":"1980-10-10"
        }
}'
```

### Simple example data
```JSON
{
    "order":{
            "name":"Scandinavium 1980-10-10",
            "delivery_group":"Smallwood DG",
            "order_type":"delivery",
            "scheduled_date":"1980-10-10"
        }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "order": {
        "name": "Scandinavium 1980-10-10",
        "order_type": "DELIVERY",
        "scheduled_date": "1980-10-10",
        "created_date": "1980-10-10 08:44:22",
        "delivery_group": "Smallwood DG",
        "status": "NOT_STARTED",
        "num_customers": 0
    }
}'
```

### Advanced example data
```JSON
{
    "order": {
        "name": "Scandinavium 1980-10-10",
        "order_type": "DELIVERY",
        "scheduled_date": "1980-10-10",
        "created_date": "1980-10-10 08:44:22",
        "delivery_group": "Smallwood DG",
        "status": "NOT_STARTED",
        "num_customers": 0
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "data": "add_order2 could not be validated: [order.order_type] The property order_type is required"
}
```

### Example success response
```JSON
{
    "order": "Scandinavium 1980-10-10",
    "result": "ok",
    "status": 200,
    "data": "{order_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/Order/get/{order_id}"
}
```
