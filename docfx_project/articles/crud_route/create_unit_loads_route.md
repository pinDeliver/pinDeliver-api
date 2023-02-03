# Create route with unit loads

Used to to create unit loads on a route using a route id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/route/create_unit_loads/{route_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/route/create_unit_loads/{route_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--data-raw ''
```


### Example success response
```JSON
[]
```
