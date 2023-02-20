# Driver events

### Example

```JSON
{
  "event": "DRIVER_WAS_CREATED",
  "id": "{driver_id}",
  "url": "https://cloud.pindeliver.com/api/v1_2/driver/get/{driver_id}"
}
```

### Post data

```JSON
{
  "event": "DRIVER_WAS_CREATED",
  "id": "{driver_id}",
  "url": "http://localhost/api/v2_1/driver/get/{driver_id}"
}
```
```JSON
{
  "event": "DRIVER_WAS_UPDATED",
  "id": "{driver_id}",
  "url": "http://localhost/api/v2_1/driver/get/{driver_id}"
}
```
```JSON
{
  "event": "DRIVER_WAS_DELETED",
  "id": "{driver_id}",
  "url": "http://localhost/api/v2_1/driver/get/{driver_id}"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|DRIVER_WAS_CREATED|A driver was created|
|DRIVER_WAS_UPDATED|A driver was updated|
|DRIVER_WAS_DELETED|A driver was deleted|
