# Update customer

Used to update data on an existing customer using the customer id

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
POST
```

### Example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/update/{customer_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "customer": {
        "postal_address":"Andra Långgatan 2"
    }
}'
```

### Example data
```JSON
{
    "customer": {
        "postal_address":"Andra Långgatan 2"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such customer available"
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

---

# Update customer using external id

Used to update data on an existing customer using the customer external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/update/extid/{external_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/update/extid/{external_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "customer": {
            "postal_address": "Andra Långgatan 17",
            "zipcode": "41303",
            "city": "Göteborg"
    }
}'
```

### Example data
```JSON
{
    "customer": {
            "postal_address": "Andra Långgatan 17",
            "zipcode": "41303",
            "city": "Göteborg"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such customer available"
}
```

### Example success response
```JSON
{
    "result": "ok",
    "status": 200,
    "data": "{external_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{external_id}"
}
```

---

# Output format

### Customer Object Properties

|Property              |Type     |Description          |Example      |
|----------------------|---------|---------------------|-------------|
|customer<font color='red'>*</font>|||Details in [add_customer_order](/articles/crud_customer/add_customer_order.html) under output format|
