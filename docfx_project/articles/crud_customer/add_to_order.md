# Add to order

A customer can be added independently or as part of an existing [order](/articles/crud_order/get_order.html). If not specified, it will be added to the inbox. Use order_id if you want to specify which order it should be added to.
A customer is needed to be able to add packages. It is possible to add packages in the same request when adding a customer. See below for more details.

### Endpoint
```
https://cloud.pindeliver.com/api/v2_1/order/addCustomer/{order_id}
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
curl --location --request POST 'https://cloud.pindeliver.com/api/v2_1/order/addCustomer/{order_id}' \
--header 'X-PINDELIVER-API-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'X-PINDELIVER-API-CLIENT-KEY: XXXX-XXXX-XXXX-XXXX' \
--header 'Content-Type: application/json' \
--data-raw '{
        "customers": [
        {
            "id": {customer_id},
            "name": "Steve Harris",
            "postal_address": "Andra Långgatan 17",
            "city": "Göteborg",
            "service": {
            }
        }
    ]
}'
```

### Example data
```JSON
{
        "customers": [
        {
            "id": "{customer_id}",
            "name": "Steve Harris",
            "postal_address": "Andra Långgatan 17",
            "city": "Göteborg",
            "service": {
            }
        }
    ]
}
```

### Example error response
```JSON
{
    "result": "error",
    "status": 404,
    "data": "No such order available"
}
```

### Example success response
```JSON
[
    {
        "result": "ok",
        "data": "{customer_id}",
        "url": "https://cloud.pindeliver.com/api/v2_1/customer/get/{customer_id}"
    }
]
```

---

# Output format

### Customer Object Properties

Fields marked with <font color='red'>*</font> are required

|Property              |Type     |Description          |Example      |  
|----------------------|---------|---------------------|-------------|
|name<font color='red'>*</font>|string|Name of this costumer|Steve Harris|
|order_id|string or null|Unique id for an order. Used to coennct a costumer to a specific order|123456|
|delivery_group|string or null|Delivery group identifier. The delivery group must exist in pinDeliver, otherwise an error will be returned|Smallwood Group|
|customer_number|string or null|Unique user id/customer number|ABC001|
|language_code|string or null|Decides which language that is used on the customer page|sv_SE|
|postal_address<font color='red'>*</font>|string|Customer address. Street address and number only|Rosenlundsgatan 7|
|address_2|string or null|c/o, apartment number or similar|Rosenlundsgatan 3|
|zipcode|string or null|Customer address zip code|41303|
|city<font color='red'>*</font>|string|Customer address city|Gothenburg|
|phone_cell|string or null|Customer cellphone number. Shown in driver app and used for SMS notifications|0701-12 34 56|
|phone_alt|string or null|Alternate customer phone number. Shown in driver app but NOT used for SMS notifications. Landline or cellphone accepted|031-12 34 56|
|email|string or null|Customer email address. May be used for delivery notifications|name@example.com|
|position_lat|number or null|If the latitude and longitude coordinates are supplied then pinDeliver will not try to calculate them automatically|57.700663864|
|position_lng|number or null|If the latitude and longitude coordinates are supplied then pinDeliver will not try to calculate them automatically|11.954662848|
|customer_type|string or null|Type of customer that will receive the delivery. Valid values are 'b2c' for an ordinary customer, or 'b2b' for a business to business delivery|b2b|
|service<font color='red'>*</font>||Specific information about the current customer service order|Details below|

### Service Object Properties

Fields marked with <font color='red'>*</font> are required

|Property          |Type     |Description          |Example      |  
|------------------|---------|---------------------|-------------|
|type|string|Which type of delivery it is. Pickup or dropoff|dropoff|
|pickup_identifier|string or null|Identifier used to connect a pikcup to a dropoff|Pickup-3|
|external_sender_id|string or null|Id that match customer id in the commerce system of the transporter|1 OR 101 OR 976|
|sms_sender|string or null|Name of the sender of a SMS. Minimum 3, and maximum length of 11 characters. Only alphanumeric characters (A-Z and 0-9) are allowed, and first character must be a letter|pinDeliver|
|sender_name|string or null|Customer friendly name to be used inside SMS messages|pinDeliver AB|
|packages_replace|boolean or null|Used to indicate if it is okay to replace packages on delivery or not|false|
|weight|number or null|If provided together with vehicle max capacity (set in admin web interface) this value represents the consumed vehicle weight for the specific delivery. If used, the same unit type/scale must be used in vehicle settings. Used in route optimization|43|
|volume|number or null|If provided together with vehicle max capacity (set in admin web interface) this value represents the consumed vehicle volume for the specific delivery. If used, the same unit type/scale must be used in vehicle settings. Used in route optimization|32|
|volume_2|number or null|If provided together with vehicle max capacity (set in admin web interface) this value represents the consumed vehicle volume for the specific delivery. If used, the same unit type/scale must be used in vehicle settings. Used in route optimization|23|
|tracking_number|string or null|Tracking number for delivery|1 or a101 or ABC-976|
|hub_id|string or null|Hub id for delivery|1 or a101 or ABC-123|
|reference|string or null|Text fron another system. Used to reference between systems|Reference123|
|delivery_category|string or null|Generic label, used for grouping deliveries||
|vehicle_tags|string or null|Tags used for pairing delivery with specific vehicle(s)|Eco1,Eco2|
|timewindow_start|string or null|If provided, this value will dictate the opening time window for delivering to the customer when the route is being optimized. (i.e. the earliest time a delivery can be made)|14:30|
|timewindow_end|string or null|If provided, this value will dictate the closing time window for delivering to the customer when the route is being optimized. (i.e. the latest time a delivery can be made)|19:30|
|driver_note_1|string or null|Additional customer information such as directions, door codes, or other relevant delivery instructions|The only red house on the street|
|driver_note_2|string or null|Additional customer information such as directions, door codes, or other relevant delivery instructions|Door code 1234|
|driver_note_3|string or null|Additional customer information such as directions, door codes, or other relevant delivery instructions|Leave package outside if we are not at home|
|internal_note|string or null|Internal customer information such as relevant delivery instructions|Use the second door, no answer on the first one|
|stop_time|integer or null|Amount of time allocated for each PICKUP/DELIVERY - specified in minutes|5|
|requested_delivery_date|string or null|Informational field for requested delivery date in ISO 8601 format. This date is NOT used when routing|1980-10-10|
|age_verification|integer or null|If the delivery includes age restricted items, this field indicates the recipients minimum allowed age. If set, this value will be shown in the driver app. The driver will be prompted to perform an identity check before delivering the items to the customer|18|
|priority|string or null|Priority in optimization. LOW, NORMAL, HIGH. Normal is default|HIGH|
|unattended_ok|boolean or null|Used to indicate if a delivery can be made if the costumer is not home|true|
|packages||Specific information about the current customer package|Details below|

### Packages Object Properties

Fields marked with <font color='red'>*</font> are required

|Property              |Type     |Description          |Example      |  
|----------------------|---------|---------------------|-------------|
|name|string|Name of the package type. Shown in driver app and exported excel driver sheet|Fender Precision|
|quantity|integer|Number of packages of this type. Shown in driver app and exported excel driver sheet|20|
|is_article|boolean||false|
|shared|boolean|Used to indicate if a package is a shared package or not|false|
|weight|number or null|The weight of a specific package|5,5|
|volume|number or null|The volume of a specific package|7,8|
|volume_2|number or null|The volume of a specific package|35|
|package_id|string or null|An external id for this package|S-67895674|
|shipment_number|string or null|An external number for the shipment|123456789|
|url|string or null|A url linking to a page with information about the package, e.g. a product image|https://pindeliver.com	|
|packaging_type|string or null|The kind of packaging type the package is|Srs-back|
|dangerous_goods||Specific information about the current customer packages dangerous goods|Details below|

### Dangerous goods Object Properties

Fields marked with <font color='red'>*</font> are required

|Property              |Type     |Description          |Example      |  
|----------------------|---------|---------------------|-------------|
|adr_points|integer or null|ADR classifies dangerous goods into different categories based on the nature of the hazard they pose, and establishes regulations for the packaging, labeling, and transportation of these goods.|198|
|un_number|string or null|The UN Number is used globally to identify and classify hazardous materials, including chemicals, explosives, flammable liquids and gases, toxic substances, and radioactive materials|3262|
|marine_pollutant|boolean or null|Marine pollutants are dangerous substances that pose a risk to the marine environment during transportation by sea|true|
|article_number|string or null|The article number of the dangerous goods|D-000378|
|flash_point|integer or null|The flash point of flammable liquids determines their fire hazard and helps classify and regulate their storage and transportation|70|
