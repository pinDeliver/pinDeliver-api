# Events

pinDeliver operates on an event-based system, meaning that whenever certain actions take place in the system, event messages are sent to preconfigured event listeners. These events are given specific names that identify the object involved and the type of action that has occurred. For example, the event ROUTE_WAS_LOCKED is triggered when a route is locked by a transport leader. The event message also includes the pinDeliver ID for the object in question.

Listeners can use this information to decide whether they need to retrieve the object and update their own records with the latest information. This approach has many practical applications. For instance, it could be used to update the estimated time of arrival (ETA) in a business system or to set the delivery sequence in a warehouse management system (WMS) to optimize the picking order.

Overall, pinDeliver's event-based architecture offers a flexible and efficient way to keep different systems synchronized and up-to-date with the latest information.

![Flowchart](../images/flowchart_all.jpg)
