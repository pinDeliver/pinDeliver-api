# Update delivery group

JSON Schema for updating Delivery group API

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/delivery_group/update/{delivery_group_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/delivery_group/update/{delivery_group_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "delivery_group": {

       "name": "Smallwood DG"
    }
}'
```

### Example data
```JSON
{
    "delivery_group": {

        "name": "Smallwood DG"
    }
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 400,
    "response": {
        "error_description": "Request must contain valid json"
    }
}
```

### Example success response
```JSON
{
    "delivery_group": "Smallwood DG",
    "result": "ok",
    "code": 200,
    "data": "{delivery_group_id}",
    "url": "https://cloud.pindeliver.com/api/v2_1/delivery_group/get/{delivery_group_id}"
}
```

---

# Input format

### Delivery Group object properties

Fields marked with <font color='red'>*</font> are required

|Property|Type|Description|Example|
|--------|----|-----------|-------|
|delivery group<font color='red'>*</font>|||Details in [add delivery group](/articles/crud_delivery_group/add_delivery_group.html) under output format|
