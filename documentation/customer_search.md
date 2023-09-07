# Search customer

Used to search for a customer. Two search parameters are needed

### Endpoint
```
https://cloud.pindeliver.com/api/v2_0/customer/search
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_0/customer/search' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name": "Anders Andersson",
    "city": "Göteborg"

}'
```

### Example data
```JSON
{
    "name": "Anders Andersson",
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
          "delivery_group": "DeliveryGroup",
          "name": "Anders Andersson",
          "language_code": "sv_SE",
          "postal_address": "Andra Långgatan 17",
          "zipcode": "",
          "city": "Göteborg",
          "country_code": "",
          "phone_cell": "",
          "position_lat": 57.69925,
          "position_lng": 11.9489155,
          "url": "https://cloud.pindeliver.com/api/v2_0/customer/get/{customer_id}",
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

---

# Input format

### Search Object Properties

At least 2 search fields are required

|Property              |Type     |Description          |Example      |Default|
|----------------------|---------|---------------------|-------------|-------|
|name|string|The customers first and last name|John Doe|NULL|
|external_sender_id|string|Unique identifier for sender|pinDeliver|NULL|
|requested_delivery_from_date|string|The customers requested_delivery_date must be equal to or greater then from_date.|YYYY-mm-dd|NULL|
|requested_delivery_to_date|string|The customers requested_delivery_date must be equal to or less then from_date.|YYYY-mm-dd|NULL|
|phone_cell|string|Customer cellphone number.|0701-12 34 56|NULL|
|email|string|Customer email address.|name@example.com|NULL|
|city|string|Customer address city.|Göteborg|NULL|
|postal_address|string|Customer postal address street|Nils Ericsonsplatsen 3|NULL|
|zipcode|string|Customer address zip code.|41103|NULL|
|order_id|integer|Search only customers who belong to an order.|1337|NULL|
|hub_id|string|Search only customers who belong to hub.|1 or a101 or ABC-123|NULL|
|stop_type|enum|Search only customers who have stop_type.|dropoff or pickup or collect|NULL|
|vehicle_tags|string|Tags used for pairing delivery with specific vehicle(s).|NULL|
|timewindow_from|string|The customers requested timewindow start.|HH:ii|NULL|
|timewindow_to|string|The customers requested timewindow end.|HH:ii|NULL|
|pickup_identifier|string|Search only customers who share the same pickup point.|ABC-123|NULL|
|customer_number|string|The customers customer_number.|123abc|NULL|
|reference|string|The customers reference.|abc123|NULL|
