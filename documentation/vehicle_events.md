# Vehicle events

### Example

```JSON
{
  "event": "VEHICLE_WAS_UPDATED",
  "id": "{vehicle_id}",
  "url": "https://localhost/api/v2_0/vehicle/get/{vehicle_id}",
    "external_id": "B1"
}
```

### Post data


```JSON
{  
  "event": "VEHICLE_WAS_CREATED",
  "id": "<vehicle-id>",
  "url": "<api-2.0-url for vehicle>",
  "external_id": "<external_id>"
}
```
```JSON
{  
  "event": "VEHICLE_WAS_DELETED",
  "id": "<vehicle-id>",
  "url": "<api-2.0-url for vehicle>",
  "external_id": "<external_id>"
}
```
```JSON
{  
  "event": "VEHICLE_WAS_UPDATED",
  "id": "<vehicle-id>",
  "url": "<api-2.0-url for vehicle>",
  "external_id": "<external_id>"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|VEHICLE_WAS_CREATED|A vehicle was created|
|VEHICLE_WAS_DELETED|A vehicle was deleted|
|VEHICLE_WAS_UPDATED|A vehicle was updated|
