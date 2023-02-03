# Vehicle events

### Example



### Post data


```JSON
{  
  "event": "VEHICLE_WAS_CREATED",
  "id": "<vehicle-id>",
  "url": "<api-2.1-url for vehicle>"
}
```
```JSON
{  
  "event": "VEHICLE_WAS_DELETED",
  "id": "<vehicle-id>",
  "url": "<api-2.1-url for vehicle>"
}
```
```JSON
{  
  "event": "VEHICLE_WAS_UPDATED",
  "id": "<vehicle-id>",
  "url": "<api-2.1-url for vehicle>"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|VEHICLE_WAS_CREATED|A vehicle was created|
|VEHICLE_WAS_DELETED|A vehicle was deleted|
|VEHICLE_WAS_UPDATED|A vehicle was updated|
