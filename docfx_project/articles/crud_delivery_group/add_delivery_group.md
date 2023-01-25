# Add delivery group

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/delivery_group/add
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

### Simple example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/delivery_group/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "delivery_group": {

            "name": "Smallwood DG",
            "identifier": "Smallwood DG"
    }
}
'
```

### Simple example data
```JSON
{
    "delivery_group": {

            "name": "Smallwood DG",
            "identifier": "Smallwood DG"
    }
}
```

### Advanced example request
```C
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/delivery_group/add' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "delivery_group": {

            "name": "Smallwood Group",
            "identifier": "Smallwood Identifier",
            "base_stop_time": "5",
            "apartment_stop_time": "7",
            "depot_reload_time_minutes": "5",
            "depot_address": "Valhallavägen 1, 41251 Göteborg",
            "depot_location_latitude": "57.699312",
            "depot_location_longitude": "11.987573"
    }
}
'
```

### Advanced example data
```JSON
{
    "delivery_group": {

            "name": "Smallwood Group",
            "identifier": "Smallwood Identifier",
            "base_stop_time": "5",
            "apartment_stop_time": "7",
            "depot_reload_time_minutes": "5",
            "depot_address": "Valhallavägen 1, 41251 Göteborg",
            "depot_location_latitude": "57.699312",
            "depot_location_longitude": "11.987573"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "'name' is required"
    }
}
```

### Example success response
```JSON
{
    "delivery_group": "Smallwood Group",
    "result": "ok",
    "code": 200,
    "data": "{delivery_group_id}",
    "url": "https://cloud.pindeliver.com/api/v2_0/delivery_group/get/745"
}
```
