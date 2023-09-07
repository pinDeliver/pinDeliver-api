# Delivery group events

### Example

```JSON
{
  "event": "DELIVERY_GROUP_WAS_UPDATED",
  "id": "{delivery_group_id}",
  "url": "https://cloud.pindeliver.com/api/v2_0/delivery_group/get/{delivery_group_id}",
  "external_id": "DeliveryGroup"
}
```

### Post data

```JSON
{
  "event": "DELIVERY_GROUP_WAS_UPDATED",
  "id": "{delivery_group_id}",
  "url": "<api-2.0-url for delivery group>",
  "external_id": "DeliveryGroup"
}
```
```JSON
{
  "event": "DELIVERY_GROUP_WAS_DELETED",
  "id": "{delivery_group_id}",
  "url": "<api-2.0-url for delivery group>",
  "external_id": "DeliveryGroup"
}
```
```JSON
{
  "event": "DELIVERY_GROUP_WAS_CREATED",
  "id": "{delivery_group_id}",
  "url": "<api-2.0-url for delivery group>",
  "external_id": "DeliveryGroup"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|DELIVERY_GROUP_WAS_UPDATED|A delivery group was updated|
|DELIVERY_GROUP_WAS_DELETED|A delivery group was deleted|
|DELIVERY_GROUP_WAS_CREATED|A delivery group was created|
