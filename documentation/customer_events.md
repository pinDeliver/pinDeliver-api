# Customer events

### Example

```JSON
{
  "event": "CUSTOMER_WAS_DELETED",
  "id": "{customer_id}",
  "external_id": "{external_id}"
}
```
```JSON
{
  "event": "DELIVERY_WAS_COMPLETED",
  "id": "{customer_id}",
  "url": "https://localhost/api/v2_1/Order/getCustomer/{customer_id}",
  "external_id": "{external_id}"
}
```


### Post data
```JSON
{  
  "event": "DELIVERY_WAS_COMPLETED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{  
  "event": "CUSTOMER_WAS_CANCELLED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{  
  "event": "CUSTOMER_WAS_UNCANCELLED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event":"CUSTOMER_WAS_MERGED",
  "id":"<source-order-delivery-id>",
  "target_id":"<target-order-delivery-id>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event":"CUSTOMER_WAS_REBOOKED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event":"CUSTOMER_WAS_DELETED",
  "id": "<order-delivery-id>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event": "DRIVER_IS_APPROACHING_CUSTOMER",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event": "DRIVER_HAS_ARRIVED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event": "CUSTOMER_RELOCATION_TASK_WAS_CREATED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```
```JSON
{
  "event": "CUSTOMER_RELOCATION_TASK_WAS_COMPLETED",
  "id": "<order-delivery-id>",
  "url": "<api-2.1-url for order-delivery>",
  "external_id": "<external_id>"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|DELIVERY_WAS_COMPLETED|A delivery was completed|
|CUSTOMER_WAS_CANCELLED|A customer delivery was cancelled|
|CUSTOMER_WAS_UNCANCELLED|A customer delivery was uncancelled|
|CUSTOMER_WAS_MERGED|A customer was merger with another customer|
|CUSTOMER_WAS_REBOOKED|A customer was rebooked to another starting time|
|CUSTOMER_WAS_DELETED|A customer was deleted|
|DRIVER_IS_APPROACHING_CUSTOMER|A driver is approaching a customer|
|DRIVER_HAS_ARRIVED|A driver has arrived at a customer|
|CUSTOMER_RELOCATION_TASK_WAS_CREATED|A relocation task to relocate packages from one customer to another was created|
|CUSTOMER_RELOCATION_TASK_WAS_COMPLETED|A relocation task to relocate packages from one customer to another was completed|
