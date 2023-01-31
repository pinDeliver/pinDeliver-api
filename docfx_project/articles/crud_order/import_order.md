# Import order

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/order/import
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/import' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
  "order": {
    "name": "Scandinavium 1980-10-10",
    "order_type": "DELIVERY",
    "scheduled_date": "1980-10-10",
    "delivery_group": "Smallwood DG"
  }
}'
```

### Simple example data
```JSON
{
  "order": {
    "name": "Scandinavium 1980-10-10",
    "order_type": "DELIVERY",
    "scheduled_date": "1980-10-10",
    "delivery_group": "Smallwood DG"
  }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/import' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "order": {
        "name": "Scandinavium 1980-10-10",
        "order_type": "DELIVERY",
        "scheduled_date": "1980-10-10",
        "created_date": "1980-10-10 13:52:53",
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
        "created_date": "1980-10-10 13:52:53",
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
    "data": "add_order2 could not be validated: [order.delivery_group] The property delivery_group is required"
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
