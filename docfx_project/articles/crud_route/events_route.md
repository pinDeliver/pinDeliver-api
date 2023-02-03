# Route events

### Example



### Post data
```JSON
{  
  "event": "ROUTE_WAS_LOCKED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_UNLOCKED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_ASSIGNED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_UNASSIGNED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_STARTED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "ROUTE_WAS_COMPLETED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
}
```
```JSON
{  
  "event": "LOADING_WAS_COMPLETED",
  "id": "<route-id>",
  "url": "<api-1.2-url for route>"
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
