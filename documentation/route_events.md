# Route events

### Example

```JSON
{
  "event": "ROUTE_WAS_LOCKED",
  "id": "{route_id}",
  "url": "https://localhost/api/v2_0/Route/get/{route_id}"
}
```
```JSON
{
  "event": "LOADING_WAS_COMPLETED",
  "id": "{route_id}",
  "subroute_number": 1,
  "url": "https://localhost/api/v2_0/Route/get/{route_id}"
}
```

### Post data
```JSON
{  
  "event": "ROUTE_WAS_LOCKED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_UNLOCKED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_ASSIGNED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_UNASSIGNED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_STARTED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_COMPLETED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "LOADING_WAS_COMPLETED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_JOURNAL_WAS_UPDATED",
  "id": "<route-id>",
  "url": "<api-2.0-url for route>"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|ROUTE_WAS_LOCKED|A route was locked|
|ROUTE_WAS_UNLOCKED|A route was unlocked|
|ROUTE_WAS_ASSIGNED|A route was assigned to a driver|
|ROUTE_WAS_UNASSIGNED|A route was unassigned from a driver|
|ROUTE_WAS_STARTED|A route was started|
|ROUTE_WAS_COMPLETED|A route was completed|
|LOADING_WAS_COMPLETED|The loading of a route was completed|
|ROUTE_JOURNAL_WAS_UPDATED|The journal of a route was updated|
