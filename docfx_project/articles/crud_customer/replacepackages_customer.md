# Replace packages

Used to replace packages on an existing customer using the customer id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/replacePackages/{customer_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/replacePackages/{customer_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "packages": [
        {
            "name": "Fender precision",
            "quantity": 1,
            "package_id": "B2",
            "status_code": "LOADED_FOR_DISTRIBUTION",
            "packaging_type_locked": true,
            "packaging_type": "Kolli"
        }
    ]
}'
```

### Example data
```JSON
{
    "packages": [
        {
            "name": "Fender precision",
            "quantity": 1,
            "package_id": "B2",
            "status_code": "LOADED_FOR_DISTRIBUTION",
            "packaging_type_locked": true,
            "packaging_type": "Kolli"
        }
    ]
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

# Replace packages using external id

Used to replace packages on an existing customer using the customer external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/replacePackages/extid/{external_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/replacePackages/extid/{external_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "packages": [
        {
            "name": "Fender precision",
            "quantity": 4,
            "package_id": "B6",
            "status_code": "LOADED_FOR_DISTRIBUTION",
            "packaging_type_locked": false,
            "packaging_type": "Kolli"
        }
    ]
}'
```

### Example data
```JSON
{
    "packages": [
        {
            "name": "Fender precision",
            "quantity": 4,
            "package_id": "B6",
            "status_code": "LOADED_FOR_DISTRIBUTION",
            "packaging_type_locked": false,
            "packaging_type": "Kolli"
        }
    ]
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

# Output format

### Customer Object Properties

|Property              |Type     |Description          |Example      |  
|----------------------|---------|---------------------|-------------|
|packages<font color='red'>*</font>|||Details in [update package](/articles/crud_package/update_package.html) under output format|
