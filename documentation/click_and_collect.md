API

docfx init -q
docfx "C:\temp\pinDeliver-api\docfx_project\docfx.json" --serve

Såhär gör du blablabla `Exempel på JSON`

>>> Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy

Se hela flödet på en order

https://martinservera-test.pindeliver.com/ApiDocs/docs/1.2/getOrder
https://dev.azure.com/pindeliver/pinDeliver/_wiki/wikis/pinDeliver.wiki/62/Hub
https://dev.azure.com/pindeliver/pinDeliver/_git/pinDeliver-Cloud-Office?path=/api-tests/customer_14.http


Exempel på API

https://martinservera-test.pindeliver.com/api/v1_2/Order/get/:order_id

## Authentication
Headers: <br>
  X-PINDELIVER-API-KEY:XXXX-XXXX-XXXX-XXXX <br>
  X-PINDELIVER-API-CLIENT-KEY:XXXX-XXXX-XXXX-XXXX

## Method
GET

## Example request
```C
curl --location --request GET 'https://martinservera-test.pindeliver.com/api/v2_0/Order/get/{ORDER-ID}' \
--header 'X-PINDELIVER-API-KEY: {API-KEY}' \
--header 'X-PINDELIVER-API-CLIENT-KEY: {CLIENT-KEY}' \
--data-raw ''
```

## Example error response
```JSON
Error Response
[
  {
    "result": "error",
    "status": 404,
    "response": {
      "error_description": "No such order available"
    }
  }
]
```

## Example success response
```JSON
Success Response
{
  "id": "2567",
  "name": "Magazine Deliveries",
  "created_date": "2017-05-18 09:02:57",
  "scheduled_date": "2017-05-18 09:02:57",
  "order_type": "DELIVERY",
  "delivery_group": "Derry01",
  "order_info": {
    "status": "NOT_STARTED",
    "num_deliveries": 46
  },
  "routes": [
    {
      "id": "4671",
      "name": "Derry van 01",
      "locked": false,
      "assigned": false,
      "scheduled_start_time": "2017-05-18 09:41:00",
      "scheduled_start_time_from_depot": "2017-05-18 09:54:00",
      "actual_start_time": "2017-05-18 09:42:32",
      "actual_start_time_from_depot": "2017-05-18 09:56:12",
      "started": false,
      "ended": false,
      "url": "https://martinservera-test.pindeliver.com/api/v1_2/route/get/4671",
      "depot_address": "Derry's Depot, 230 High Street, TUCSON AZ 85705",
      "num_deliveries": 40,
      "num_subroutes": 2
    },
    {
      "id": "4670",
      "name": "Derry van 05",
      "locked": false,
      "assigned": false,
      "scheduled_start_time": "2017-05-18 09:54:00",
      "scheduled_start_time_from_depot": "2017-05-18 10:12:00",
      "actual_start_time": "2017-05-18 09:52:32",
      "actual_start_time_from_depot": "2017-05-18 10:11:48",
      "started": false,
      "ended": false,
      "url": "https://martinservera-test.pindeliver.com/api/v1_2/route/get/4670",
      "depot_address": "Derry's Depot, 230 High Street, TUCSON AZ 85705",
      "num_deliveries": 12,
      "num_subroutes": 1
    },
    {
      "id": "4669",
      "name": "Derry van 03",
      "locked": true,
      "assigned": true,
      "scheduled_start_time": "2017-05-18 09:56:00",
      "scheduled_start_time_from_depot": "2017-05-18 10:11:00",
      "actual_start_time": null,
      "actual_start_time_from_depot": null,
      "started": false,
      "ended": false,
      "url": "https://martinservera-test.pindeliver.com/api/v1_2/route/get/4669",
      "depot_address": "Derry's Depot, 230 High Street, TUCSON AZ 85705",
      "num_deliveries": 47,
      "num_subroutes": 3
    },
    {
      "id": "4672",
      "name": "Derry van 07",
      "locked": false,
      "assigned": false,
      "scheduled_start_time": "2017-05-18 14:00:00",
      "scheduled_start_time_from_depot": "2017-05-18 14:24:00",
      "actual_start_time": null,
      "actual_start_time_from_depot": null,
      "started": false,
      "ended": false,
      "url": "https://martinservera-test.pindeliver.com/api/v1_2/route/get/4672",
      "depot_address": "Derry's Depot, 230 High Street, TUCSON AZ 85705",
      "num_deliveries": 31,
      "num_subroutes": 2
    }
  ]
}
```


"overwrite": [
  {
    "files": [
      "apidoc/**.md"
    ],
    "exclude": [
      "obj/**",
      "_site/**"
    ]
