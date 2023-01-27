# Update package using external id

Brödtext



### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/package/update/extid/B6
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/package/update/extid/B6' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "quantity": 10,
    "status_code": "PICKED_AT_TERMINAL"    
}'
```

### Example data
```JSON
{
    "quantity": 10,
    "status_code": "PICKED_AT_TERMINAL"    
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 405,
    "data": "Method Not Allowed"
}
```

### Example success response
```JSON
{
    "result": "ok",
    "status": 200,
    "data": "B6",
    "package": {
        "id": "{package_id}",
        "packaging_type": "Kolli",
        "temperature_zone": "NONE",
        "is_article": false,
        "name": "Fender precision",
        "package_id": "B6",
        "quantity": 10,
        "is_shared": false,
        "packaging_type_locked": false,
        "quantity_loaded": 0,
        "status_code": "PICKED_AT_TERMINAL",
        "status_time": "2023-01-25 14:33:52"
    }
}
```

---

# Update package using scan code

Brödtext



### Endpoint
```
/api/v2_1/:package/update/scan_code/:scan_code
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/package/update/scan_code/B6' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "quantity": 5,
    "status_code": "LOADED"    
}'
```

### Example data
```JSON
{
    "quantity": 5,
    "status_code": "LOADED"    
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 405,
    "data": "Method Not Allowed"
}
```

### Example success response
```JSON
{
    "result": "ok",
    "status": 200,
    "data": "B6",
    "package": {
        "id": "{package_id}",
        "packaging_type": "Kolli",
        "temperature_zone": "NONE",
        "is_article": false,
        "name": "Fender precision",
        "package_id": "B6",
        "quantity": 5,
        "is_shared": false,
        "packaging_type_locked": false,
        "quantity_loaded": 0,
        "status_code": "LOADED_FOR_DISTRIBUTION",
        "status_time": "2023-01-25 14:35:20"
    }
}
```
