API

docfx init -q
docfx "C:\temp\pinDeliver-api\docfx_project\docfx.json" --serve

Såhär gör du blablabla `Exempel på JSON`

>>> Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy

Upplagt efter ex order och när man klickar på order kommer olika requests och när man klickar på en request kommer olika versioner

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














```C
curl --location --request POST 'https://martinservera-test.pindeliver.com/api/v1_4/customer/add' \
--header 'X-PINDELIVER-API-KEY: 1212-1212-1212-1212' \
--header 'X-PINDELIVER-API-CLIENT-KEY: 030dc9f7-9f86-11ec-b8fc-0242c0a85005' \
--header 'Content-Type: application/json' \
--data-raw '{
    "linehaul_order": true,
    "validation_request":false,
    "preliminary":false,
    "allow_adding_to_locked":false,
    "order_id":31561,
    "route_id":143762,
    "position_in_route":1,
    "name":"Linehaul",
    "postal_address":"Andra Långgatan",
    "country_code": "sv",
    "address_2":"",
    "zipcode": "41161",
    "city":"Göteborg",
    "delivery_info": {
        "stop_type":"delivery",
        "timewindow_start":"00:00",
        "timewindow_end":"23:59"
    }
}'
```

```JSON
{
    "id": 8774325,
    "delivery_type": "PICKUP",
    "delivery_group": "Beleco - Sthlm",
    "order_id": 98987,
    "route_id": 418472,
    "subroute": 1,
    "position_in_subroute": 4,
    "tracking_number": "1032669_pickup_8d926f",
    "tracking_url": "https:\/\/my.pindeliver.com\/8bollt5on9d",
    "name": "Harald Cavalli-Bj\u00f6rkman - Re:Newcell AB",
    "postal_address": "Cardellgatan 1",
    "zipcode": "11436",
    "city": "Stockholm",
    "phone_cell": "0705903204",
    "phone_alt": "",
    "position_lat": "59.3389407",
    "position_lng": "18.0755887",
    "sms_sender": "Beleco",
    "sender_name": "Beleco",
    "vehicle_tags": "",
    "external_sender_id": "Beleco",
    "delivery_info": {
        "requested_delivery_date": "2022-11-25",
        "timewindow_start": "09:00",
        "timewindow_end": "17:00",
        "estimated_service_time": 1200,
        "volume": 5.148,
        "priority": "normal",
        "time_estimated": "2022-11-25 13:35:57",
        "time_estimated_updated": "2022-11-25 14:07:42",
        "time_handled": "2022-11-25 15:51:02",
        "stop_time": 20,
        "status": "delivered",
        "handled_lat": 59.3389407,
        "handled_lng": 18.0755887,
        "stop_type": "pickup",
        "pickup_identifier": "scpi-991630142",
        "pods": [],
        "recycling": [],
        "packages": [{
            "id": 7025805,
            "name": "B2241-616831EE-4",
            "shared": false,
            "quantity": 1,
            "status_code": "DELIVERED",
            "status": "DELIVERED",
            "status_time": "2022-12-05 15:29:29",
            "quantity_loaded": 0,
            "quantity_delivered": 1,
            "deviation_code": "NONE",
            "driver_comment": ""
        }],
        "package_type": "1 st B2241-616831EE-4",
        "quantity": 1
    }
}'
```
