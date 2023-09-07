# Get Package

Used to retrieve a package using the package id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/package/get/{package_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/package/get/{package_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such package available"
    }
]
```

### Example success response
```JSON
{
    "id": "{package_id}",
    "packaging_type": "Kolli",
    "temperature_zone": "NONE",
    "is_article": false,
    "name": "Fender precision",
    "package_id": "B1",
    "quantity": 1,
    "is_shared": false,
    "packaging_type_locked": true,
    "quantity_loaded": 0,
    "status_code": "LOADED_FOR_DISTRIBUTION",
    "status_time": "2023-01-25 09:48:58"
}
```

---

# Get Package using external id

Used to retrieve a package using the package external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/package/get/extid/b1
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/package/get/extid/b1' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such package available"
    }
]
```

### Example success response
```JSON
{
    "id": "{package_id}",
    "packaging_type": "Kolli",
    "temperature_zone": "NONE",
    "is_article": false,
    "name": "Fender precision",
    "package_id": "B1",
    "quantity": 1,
    "is_shared": false,
    "packaging_type_locked": true,
    "quantity_loaded": 0,
    "status_code": "LOADED_FOR_DISTRIBUTION",
    "status_time": "2023-01-25 09:48:58"
}
```

---

# Get Package using scan code

Used to retrieve a package using a scan code

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/package/get/scan_code/B6
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/package/get/scan_code/B6' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such package available"
    }
]
```

### Example success response
```JSON
{
    "id": "{package_id}",
    "packaging_type": "Kolli",
    "temperature_zone": "NONE",
    "is_article": false,
    "name": "Fender precision",
    "package_id": "B6",
    "quantity": 4,
    "is_shared": false,
    "packaging_type_locked": false,
    "quantity_loaded": 0,
    "status_code": "LOADED_FOR_DISTRIBUTION",
    "status_time": "2023-01-25 14:27:53"
}
```

---

# Query parameters

### Endpoint example
```
https://cloud.pindeliver.com/api/v2_0/package/get/{package_id}?all
```

If you want to use multiple parameters at the same time you can add them after the first parameter using "&".
For example: ?all&order&routes.

### Parameters

|Property|Description|
|--------|-----------|
|?all|Get all info for the specific package|
|?order|Get orders for the specific package|
|?routes|Get routes for the specific package|
|?stops|Get stops for the specific package|
|?customer|Get customers for the specific package|
