# Update package using external id

Used to update a package using the package external id

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

Used to update a package using a scan code

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

---

# Output format

### Package Object Properties

Fields marked with <font color='red'>*</font> are required

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|packages<font color='red'>*</font>||Specific information about the current customer package|Details below|

Fields marked with <font color='red'>*</font> are required

|Property             |Type     |Description          |Example      |  
|---------------------|---------|---------------------|-------------|
|name|string|Name of the package type. Shown in driver app and exported excel driver sheet.|Package|
|package_id|string or null|An external id for this package.|98765|
|quantity|integer or null|Number of packages of this type. Shown in driver app and exported excel driver sheet.|5|
|quantity_loaded|integer or null|The quantity of loaded packages|3|
|quantity_delivered|integer or null|The quantity of packages delivered|2|
|weight|number or null|The weight of a specific package|17|
|volume|number or null|The volume of a specific package|4,5|
|volume_2|number or null|The volume of a specific package|6,5|
|shipment_number|string or null|An external number for the shipment|999|
|url|string or null|A url linking to a page with information about the package, e.g. a product image.|https://pindeliver.com|
|status_code|string or null|The status of a specific package|ARRIVED_AT_TERMINAL|
|status_time|string or null|The time the package got it's latest status|1980-10-10 13:54:19|
|packaging_type_identifier|string or null|The kind of packaging type the package is|Srs-back|
|packaging_type_id|integer or null|The id of the packaging type|12345|
