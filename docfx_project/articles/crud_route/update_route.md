# Update route

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/update/{route_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/Route/update/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "route": [
        {
            "scheduled_start_time": "2023-01-25 21:00:00",
            "scheduled_end_time": "2023-01-25 23:47:21"
        }
    ]
}'
```

### Example data
```JSON
{
    "route": {
            "scheduled_start_time": "2023-01-25 21:00:00",
            "scheduled_end_time": "2023-01-25 23:47:21"
        }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such route available",
    "exec_time": 0.034607887268066406
}
```

### Example success response
```JSON
{
    "route": "Ed force one",
    "result": "ok",
    "status": 200,
    "data": "{route_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/Route/get/{route_id}",
    "exec_time": 0.05251193046569824
}
```
