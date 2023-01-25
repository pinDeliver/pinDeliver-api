# Search customer

Brödtext

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/customer/search
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/customer/search' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name": "Steve Harris",
    "city": "Göteborg"

}'
```

### Example data
```JSON
{
    "name": "Steve Harris",
    "city": "Göteborg"

}
```

### Example error response
```JSON

```

### Example success response
```JSON
{
    "customer": [
        {
          "id": "{customer_id}",
          "order_id": "{order_id}",
          "delivery_group": "Smallwood DG",
          "name": "Steve Harris",
          "language_code": "sv_SE",
          "postal_address": "Andra Långgatan 17",
          "zipcode": "",
          "city": "Göteborg",
          "country_code": "",
          "phone_cell": "",
          "position_lat": 57.69925,
          "position_lng": 11.9489155,
          "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}",
          "service": {
              "type": "dropoff",
              "sms_sender": "Ovning",
              "sender_name": "pinDeliver",
              "recycling": [],
              "packages": [],
              "tracking_number": "",
              "vehicle_tags": "",
              "timewindow_start": "01:01",
              "timewindow_end": "23:15",
              "requested_delivery_date": "2023-01-23",
              "priority": "normal",
              "tracking_url": "https://my.pindeliver.com/8ou0gosih8h"
          },
          "customer_type": "b2c"
      }
  ]
}
```
