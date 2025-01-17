---
title: Backlog Strategy
description: >-
    Many, if not most, teams using backlogs are doing so inefficiently.
weight: 2
---

Nearly all teams I have been assigend to help with their delivery issues use their backlogs incorrectly. THey are trying to mix two different types of activites into one tracking strategy and this has always proved difficult. Succesful teams have two tyeprse of activities they perform. One is deliverying value through theiur product and the other is the work required in the deliverance of that value to the customer. Teams need to rack Work and Value.

## Work And Value

THe primary purpose of the team is to deliver value. They were not established to write code, or manage a database. THey were brought together to deliver value to the customer.

For software development teams, delivering value means witing code and deploying a compiled artifact into a production execution environment. THese teams deal with adding features and addressing defects. Their activities are coordinated in a product backlog and teams deliver backlog items.

For some teams, delivering value means performing work on behalf of the customers. Operations teams tend to delivery value by configuring systes, backing up data and performing services for the customer. These teams deal with providing services to the customer, not a physical artifact. Serivce teams coordinate their activities in service queues and historically work "tickets" in those queues.

### Backlog Items and Service Tickets

Other teams, many adopting both development and operations (i.e., "DevOps") deal with both. They work both tickets from service queues and items (features and defects) from product backlogs. As more product teams take on both development and operations, their product backlog start to contain both service tickets and backlog items, Since service tickets and backlog items track different things and require different management practices, using one tool and process leads to innefiencies.

### Fit for Purpose
Teams are given a tool and told to manage their backlog with it. While this is fundamentally the tool dictating the process, it is a fact of life for most teams to use the corporate standard tool sets.

Managing a product backlog is different from managing service queues. Using one tool to handle two different activities does not work well. Trying to manage backlogs with a service management tool is is not a good fit. They use different idioms and concepts. ServiceNow struggled with this when it introduced it "agile" module. It to nearly 10 years to get it right. Atlassian discovered this when it tried to manage service queues in their Jira product. It eventually introduced another product to specifically handle service management functions.

When product teams need to handle both backlog items and serive tickets, they eventually settlon on two separate tools, each fit for thier specific purpose.

## Value Tracking Strategy - Product Backlog

THe product baclog tacks value delivers in the form of features and defects.

THe product backlog is business-facing and represnets the value of the product.

The product owner manages the product backlog and has the final say in its contensts (scope) and priority.

Customer requests are received by the product owner and placed in the backlog. The requests are refined into deliverable increments. Customer feedback is also logged in the product backlog in the form of defects, and new features. If the feature is less than expected, a new feature request is made to update the existing feature. If the feature is far less than expected, then a defect may be logged for the team to address.

Team builds processes focused on delivering value and thier tool facilitates tracking value delivery.

## Work Tracking Strategy - Service Queues

Service queues track work to be performed on behalf of the customer. Request for service are received and placed into the appropriate que based on the type of work required. Requests to restore a database may go into a database queue, while requests for adding user permissions to an application may go into an administration or configuration queue.

Service requests often have a severity associated wiit the request that is a calcualtion of data within the request ticket. For example, if the request affects thousands of users from performing a critical function it will be given a higher priority than a requires affecting one person's ability to retrieve archived data. Prioritization of work is a discrete calcualtion, not a business decision of a product manager.

Service request tickets are more difficult to predict than product backlog items. The team may open their service queues in the morning and find 500 new requests in their queues due to a network outage that occured the night previous. Compare this to a backlog item requieded by a customer. it urgance is not the same level as a service request. Even defects, when discovered in production, are more managable than a potentil storm of requests triggerd by unforseen external factors.

### Service Management Tools

Information Technology Service Management (ITSM) is a set of practices and processes that help organizations design, deliver, manage, and improve IT services to meet the needs of customers. ITSM focuses on aligning IT services with the needs of the business, improving efficiency, and delivering value to customers. 

ITSM encompasses a broader set of practices and processes beyond backlog management, including incident management, change management, problem management, service level management, and more. While backlog management is specific to managing tasks within a project, ITSM is a comprehensive approach to managing IT services across the organization to ensure alignment with business goals and delivering value to customers.


Service request tickets are unpredictable and more difficult to plan and manage. Service management tools take into account these differences and service teams choose tools to most efficently manage service requests.

While some teams have been successful breaking a backlog in two; a product backlog and a separate team backlog, service management and product management track differing things.

