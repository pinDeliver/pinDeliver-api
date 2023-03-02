# Customer order

The customer order API allows for a variety of actions, including adding, retrieving, deleting, and updating customer order information, as well as searching for specific customer orders and managing packages associated with them. A [routing order](order.md) must be created first in order to link a customer order to it, while customer orders created without an routing order will be placed in the inbox. The API also allows for packages to be linked to a customer order, and for the connection between a customer order and a [sender](sender.md) to be established. Finally, after a [vehicle](vehicle.md) has been created and linked to a route, the API facilitates linking the customer order to that [route](route.md).

![Customer](../flowchart_customer.jpg)
