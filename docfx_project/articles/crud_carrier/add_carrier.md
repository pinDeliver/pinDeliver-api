# Create a carrier

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/carrier/add
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/carrier/add' \
--header 'X-PINDELIVER-API-KEY: 1212-1212-1212-1212' \
--header 'X-PINDELIVER-API-CLIENT-KEY: 10c94858-8978-11ec-a2e8-005056011cb5' \
--header 'Content-Type: application/json' \
--data-raw '{
    "carrier": {
        "name": "TGG",
        "identifier": "Identifier"
    }
}'
```

### Example data
```JSON
{
    "carrier": {
        "name": "TGG",
        "identifier": "Identifier"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "add_carrier2 could not be validated: [carrier.identifier] The property identifier is required"
    }
}
```

### Example success response
```JSON
{
    "vehicle": "TGG",
    "result": "ok",
    "code": 200,
    "data": "{carrier_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/carrier/get/{carrier_id}"
}
```
