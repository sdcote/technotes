---
title: Feedback Loops
description: >-
    It is an unwritten truth that agile survives only through feeback. Without it, agile fails.
weight: 1
---

## Fast Feedback

## Continuous Delivery

## Automation is Critical

## User Feedback

The longest feedback loop is the that from the customer.

If you are delivering every 6 months, it will take at least 6 months to get feedback from that user and another 6 months to deliver results on that feedback. A year long feedback loop is laughable.

Apdex (Application Performance Index) is a standard method for measuring how satisfied users are with the response time of applications. It's an open standard that was developed by a group of companies. It relates to perfromance, but from the users perspective. Consider Apdex as part of your testing strategy.

## Operational - Scaling
Your components should be able to generate feedback for your infrastructure. When compute resources start to run low, the infrastructure should react by assigning more resources.

### Vertical 
Vertical scaling is related to adding more resources to a single instance.

Adding more resources often requires an outage. Few infrastructures can allocate more memory or CPU to an instance. For this reason, vertical scaling is not the preferred scaling vector.

As demands decrease the instance can be scaled down vertically as well, but this rarely happens.

### Horizontal 

Horizontal scaling involves creating more instances to handle increaded demand.

If the system is designed for horizontal scaling, adding instances does not require an outage and can be performed without affecting the user experience. The key element is the system must be designed to allow multiple compute instances. It requires horizontally scalable scomponents to be decoupled from one another and to support stateless operation. Stateless operation simply means the component instance receives state in the request and doens not track state in the instance.

Once the demand is lowered, the number of instances is reduced.