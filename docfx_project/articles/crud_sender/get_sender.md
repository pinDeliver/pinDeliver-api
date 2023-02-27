# Get sender

Used to retrieve a sender using the sender id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/sender/get/{sender_id}
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/sender/get/{sender_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "Sender with the given id '{sender_id}' was not fond on the server"
    }
]
```

### Example success response
```JSON
{
    "sender": {
        "id": "{sender_id}",
        "external_id": null,
        "name": "pinDeliver",
        "postal_address": null,
        "zipcode": null,
        "city": null
    }
}
```

---

# Get sender using external id

Used to retrieve a sender using the sender external id

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/sender/get/extid/pinDeliver
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/sender/get/extid/pinDeliver' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example error response
```JSON
[
    {
        "result": "error",
        "status": 404,
        "data": "Sender with the given external_id 'pinDelive' was not found on the server"
    }
]
```

### Example success response
```JSON
{
    "sender": {
        "id": "{sender_id}",
        "external_id": "pinDeliver",
        "name": "pinDeliver",
        "postal_address": null,
        "zipcode": null,
        "city": null
    }
}
```

---

# Get all senders

Used to retrieve all senders

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/sender/get
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
curl --location --request GET 'https://cloud.pindeliver.com/api/v2_1/sender/get' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX'
```

### Example success response
```JSON
{
    "senders": [
        {
            "id": "{sender_id}",
            "external_id": null,
            "name": "pinDeliver",
            "postal_address": null,
            "zipcode": null,
            "city": null
        }
    ]
}
```
