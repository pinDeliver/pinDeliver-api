# Get delivery group

Used to retrieve a delivery group using the delivery group id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/delivery_group/get/{delivery_group_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/delivery_group/get/{delivery_group_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "response": {
        "error_description": "Can not find such a delivery group"
    }
}
```

### Example success response
```JSON
{
    "delivery_group": {
        "id": "{delivery_group_id}",
        "name": "Smallwood Group",
        "identifier": "Smallwood Identifier",
        "base_stop_time": 5,
        "apartment_stop_time": 7,
        "depot_reload_time_minutes": 5,
        "depot_address": "Valhallavägen 1, 41251 Göteborg",
        "depot_location_latitude": 57.699312,
        "depot_location_longitude": 11.987573,
        "url": "https://cloud.pindeliver.com/api/v2_1/delivery_group/get/{delivery_group_id}"
    }
}
```

---

# Get all delivery groups

Used to retrieve all delivery groups

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/delivery_group/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/delivery_group/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```

### Example success response
```JSON
{
    "delivery_groups": [
        {
          "id": "{delivery_group_id}",
          "name": "Smallwood DG",
          "identifier": "Smallwood DG",
          "base_stop_time": 5,
          "apartment_stop_time": 7,
          "depot_reload_time_minutes": 5,
          "depot_address": "Valhallavägen 1, 41251 Göteborg",
          "depot_location_latitude": 57.699312,
          "depot_location_longitude": 11.987573,
          "url": "https://cloud.pindeliver.com/api/v2_1/delivery_group/get/{delivery_group_id}"
        }
    ]
}
```
