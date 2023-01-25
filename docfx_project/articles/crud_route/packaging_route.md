# Packaging route

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/packaging/{route_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/route/packaging/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such route available"
    }
]
```

### Example success response
```JSON
[
    {
        "packaging_type": null,
        "quantity": 24,
        "quantity_assigned": 0,
        "unit_load_type": null,
        "quantity_per_unit_load": null,
        "unit_loads": []
    }
]
```
