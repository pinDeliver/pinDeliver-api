# Retrieve a carrier

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/carrier/get/{carrier_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/carrier/get/{carrier_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "can't find carrier on server {carrier_id}"
    }
}
```

### Example success response
```JSON
{
    "carrier": {
        "id": "{carrier_id}",
        "identifier": "Identifier",
        "name": "TGG"
    }
}
```

# Get carrier using external id

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/carrier/get/extid/Identifier
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/carrier/get/extid/Identifier' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "No such carrier"
    }
}
```

### Example success response
```JSON
{
    "carrier": {
        "id": "{carrier_id}",
        "identifier": "Identifier",
        "name": "TGG"
    }
}
```

# Get all carriers

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/carrier/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_0/carrier/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example success response
```JSON
{
    "carriers": [
        {
            "id": "{carrier_id}",
            "identifier": "Identifier",
            "name": "TGG"
        }
    ]
}
```
