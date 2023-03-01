# Delete customer

Used to delete a customer from a route or directly from the inbox using the customer id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/delete/{customer_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/delete/{customer_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "No such customer available"
    }
]
```

### Example success response
```JSON
{
    "result": "ok",
    "status": 200,
    "data": "Removed NonRouted"
}
```
