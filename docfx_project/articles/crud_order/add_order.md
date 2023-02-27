# Add order

Make sure a [delivery group](/articles/crud_delivery_group/add_delivery_group.html) is created before creating an order.
You need to create an order before being able to create a [route](/articles/crud_route/add_route.html).

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
            "delivery_group":"DeliveryGroup",
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
            "delivery_group":"DeliveryGroup",
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
        "delivery_group": "DeliveryGroup",
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
        "delivery_group": "DeliveryGroup",
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

---

# Output format

### Order Object Properties

Fields marked with <font color='red'>*</font> are required

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|name<font color='red'>*</font>|string|Order name|Scandinavium 1980-10-10|
|delivery_group<font color='red'>*</font>|string|Delivery group identifier. The delivery group must exist in pinDeliver, otherwise an error will be returned|DeliveryGroup|
|order_type<font color='red'>*</font>|string|Order type identifier which can be either DELIVERY or PICKUP. If set to PICKUP the stop_time will automatically be set to 0|DELIVERY|
|scheduled_date<font color='red'>*</font>|string|The scheduled date for the delivery in ISO 8601 format|1980-10-10|
|customer|||Details in [add customer order](/articles/crud_customer/add_customer_order.html) under output format|
