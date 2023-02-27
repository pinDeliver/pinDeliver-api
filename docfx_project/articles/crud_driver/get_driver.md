# Get driver

Used to retrieve a driver using the driver id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/driver/get/{driver_id}
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
curl --location 'https://martinservera-test.pindeliver.com/api/v2_1/driver/get/{driver_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data ''
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "Not Found"
    }
}
```

### Example success response
```JSON
{
    "driver": {
        "id": "{driver_id}",
        "name": "Anders Andersson",
        "phone": "0700000000",
        "email": "email@email.com",
        "language_code": "sv_SE",
        "premium_scanning": false,
        "delivery_groups": [
            {
                "id": "{delivery_group_id}",
                "name": "Delivery group",
                "identifier": "DeliveryGroup"
            },
            {
                "id": "{delivery_group_id}",
                "name": "Delivery group 2",
                "identifier": "DeliveryGroup2"
            }
        ],
        "carrier": {
            "id": "{carrier_id}",
            "name": "Carrier",
            "external_id": "Carrier"
        }
    }
}
```

---

# Get driver using external id

Used to retrieve a driver using the external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/driver/get/externalid
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

```

### Example data
```JSON

```

### Example error response
```JSON

```

### Example success response
```JSON

```

# Get all drivers

Used to retrieve all drivers

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/driver/get
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
curl --location 'https://martinservera-test.pindeliver.com/api/v2_1/driver/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data ''
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "Not Found"
    }
}
```

### Example success response
```JSON
{
    "driver": {
        "id": "{driver_id}",
        "name": "Anders Andersson",
        "phone": "0700000000",
        "email": "email@email.com",
        "language_code": "sv_SE",
        "premium_scanning": false,
        "delivery_groups": [
            {
                "id": "{delivery_group_id}",
                "name": "Delivery group",
                "identifier": "DeliveryGroup"
            },
            {
                "id": "{delivery_group_id}",
                "name": "Delivery group 2",
                "identifier": "DeliveryGroup2"
            }
        ],
        "carrier": {
            "id": "{carrier_id}",
            "name": "Carrier",
            "external_id": "Carrier"
        }
    }
}
```
