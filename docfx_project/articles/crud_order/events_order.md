# Order events

### Example



### Post data

```JSON
{  
  "event": "ORDER_WAS_CREATED",
  "id": "<order-id>",
  "url": "<api-1.2-url for order>"
}
```
```JSON
{  
  "event": "ORDER_WAS_DELETED",
  "id": "<order-id>",
  "url": "<api-1.2-url for order>"
}
```
```JSON
{  
  "event": "ORDER_WAS_MERGED",
  "id": "<source-order-id>",
  "target_id": "<target-order-id>",
  "url": "<api-1.2-url for target-order>"
}
```
```JSON
{  
  "event": "ALL_ROUTES_LOCKED",
  "id": "<order-id>",
  "url": "<api-1.2-url for order>"
}
```

---

# Terminology

|Property             |Description|
|---------------------|-----------|
|ORDER_WAS_CREATED|An order was created|
|ORDER_WAS_DELETED|An order was deleted|
|ORDER_WAS_MERGED|An order was merged with another order|
|ALL_ROUTES_LOCKED|All routes on an order was locked|
