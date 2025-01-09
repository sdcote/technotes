---
title: Shearing Layers
description: Different parts of a system are more dynamic than others. By grouping the parts of your system that change at the same rates, your system becomes much easier to maintain.
weight: 4
---

It seems that every system I have had the opportunity to work with had a common problem. Making a simple change often required deeply invasive changes to the system. Multiple teams had to be involved, and backlog priorities had to be carefully coordinated. A delay in delivery by one team rippled through the project, disrupting the release schedules of other teams.

Product managers and owners spent more time juggling backlog items and release schedules than managing the product.

Leadership, customer support, and sales teams were constantly frustrated when a seemingly simple request would take months to deliver. In one case, adding a field to a web page took over six months to release. That field was already on another page; it just needed to appear on another one.

The cause of this problem in all those situations was the structure of the system; its architecture.

## Rates of Change

Complex systems tend to have areas with differing rates of change. A house, for example, sits on a lot that rarely changes. The foundation on the lot might change if there are additions to the house but the lot does not change. The walls of the house might change if there are additions, but they are relatively static. The services of the house (electrical, plumbing, HVAC, etc) change more often than the structure. The paint on the wall changes more often than the walls. The furniture in the house changes more often than the paint. Understanding these shearing layers helps with the development and maintenance of the system. [[1](#1)]

The same can be said for modern information systems. The front end changes more often than the back end, so placing front-end elements in the backend server means you have to change both the front end and the back end when there are user interface changes. This often means getting both the UI team and the server involved with the change and coordinating the activities of each team (e.g., backlog priorities) of both teams to release the change.

The front end of systems tends to have a different rate of change than the back end of the system and both of these change faster than the data model. These three layers have different rates of change.

### The Big Ball of Mud

Many systems today lack a clear overall design or structure, resulting in a tangled mess of interwoven dependencies and ad-hoc solutions. These systems are difficult to maintain due to their complex interdependencies that require multiple parts of the system to be modified even for the simplest of changes. 

The term "Big Ball of Mud" was coined by Brian Foote and Joseph Yoder in their 1999 paper "Big Ball of Mud" [[2](#2)] and aptly used to describe this type of system because, much like a ball of mud, it is formless, messy, and difficult to understand or modify.

This antipattern is characterized by a system that lacks a clear overall design or structure, resulting in a tangled mess of interwoven dependencies and ad-hoc solutions. 

In a Big Ball of Mud system, there is typically no clear separation of concerns, leading to a mixing of different functionalities within the same components. This can result in code duplication, tight coupling between modules, and a lack of encapsulation. The system tends to grow organically over time, with new features and changes being added haphazardly without consideration for the overall design. As a result, maintaining and extending the system becomes increasingly difficult and error-prone, making it challenging for developers to work with and understand the codebase.

## Separation of Concerns

In information technology, "separation of concerns" is a design principle that advocates for dividing a software system into distinct sections or modules, each responsible for a specific aspect of functionality. By separating concerns, developers can isolate different responsibilities within the system, making it easier to understand, maintain, and modify the codebase.

A common example of this principle is the Model-View-Controller (MVC) architecture. In MVC, the model represents the data and business logic, the view handles the presentation layer, and the controller manages the flow of information between the model and the view. This separation allows developers to focus on specific areas of the system without being overwhelmed by the complexity of the entire application.

However the separation of concerns principle traditionally only looks at functionality. It does not take into consideration the differences in rates of change between the components. It is not enough to decompose a solution by function, it should take into account how often changes affect each component.

## Shearing Layers

To ensure stability in the solution, group together elements that change at similar rates. Changes should be localized to specific parts of the system without necessitating modifications in other systems.

Yoder and Foote’s Software Shearing Layers
> Factor your system so that artifacts that change at similar rates are together.
> —Foote & Yoder, Ball of Mud Pattern [[2](#2)]

Components that change at similar rates should be grouped to provide stability to the solution. Changing should be limited to just a portion of the system and not require systemic modifications.

{{< imgproc rate-of-change Fit "660x465" >}}
Different parts of a system change at different rates. The platform and infrastructure are relatively static while the data and source code change often.{{< /imgproc >}}

A practical example of grouping systems elements by rates of change is a common web application. Design the system so that web developers can make many changes to HTML, CSS, and JavaScript to affect most of their changes. A web server or content delivery network (CDN) is established to send all the resources to the browser. The web development team manages the resources and the CDN. This enables the team to make all the changes they need for a majority of their backlog items. Any back-end services required by the web application are designed to run on separate servers and managed by the services team that release changes to the application programming interface (API) at a different rate. 

Web developers may make production releases hourly, while the service API may make releases only every few weeks or months. The only coordination between the teams and their backlogs is the web team announcing they need a back-end change by a particular date to keep their schedule. If the API is designed properly and supports backward-compatible changes or versioning, the backend team can release the change early further easing scheduling demands.

Organizing components based on shearing layers not only helps limit changes to specific domains but also facilitates project management and development. Teams can be scaled up or down based on the pace of change, with some teams expanding to support rapid changes while others remain small and agile. For instance, a project may have a large team of web developers but only a small team of database administrators.

## Finding Shearing Layers

Look at release schedules to find shearing layers in your solution. If you find releasing a new feature requires the coordination of multiple teams, you may have discovered a potential shearing layer at the team level.

Look at your backlogs and who requires backlog items. If teams are making repeated requests of one another, there may be a component in that other team that should be moved to its own layer.

Find the teams that have to collaborate to deliver. Teams should be able to perform a majority of their work without dependencies on other teams. Find the component dependencies and move the components to the other team or another layer. 

Review the current design through the lens of the [Single Responsibility Principle](https://en.wikipedia.org/wiki/Single-responsibility_principle). When a component does too much, there is a good chance that it contains shearing layers. Even if it does not, decomposing the component will still provide benefits.

## Big Ball of Mud Smells

You might have a mud ball if:
- Changes normally require inter-team collaboration
- Simple changes take several iterations to release
- Changes are often systemic and not localized
- Release management requires the coordination of multiple teams
- High dependency between teams; One can't deliver until another team does
- Higher collaboration seems to only way to improve delivery rates
- New features gradually take longer to release signaling the organic growth of a mud ball
- Developers take longer to become familiar with the codebase
- Onboarding new developers takes longer than before
- Massive codebases; this may indicate reduced separation
- A component has too many use cases indicating a monolith.

## Case Study

Let's look at a real-world case study. 

Our application acquires data from devices deployed remotely and performs analysis and processing on the received data. Different groups of devices use different transports and protocols to communicate. Our application performs processing on the data based on customer requirements. All customers have shared requirements, but many customers want additional processing. This means we offer a core product and will regularly need to add custom processing for individual clients.

### Devices

While it is possible to communicate with the device directly, many(most) devices will communicate with a Front-End Processor (FEP) usually known as a "Head-End". Each vendor will offer a solution to connect their hardware with the customers' system. Some solution providers have their generic head end to talk with other devices.

While devices themselves don’t change (with regards to firmware capabilities) the number and versions will. 20k devices may support one version of the protocol and the next 30k devices may support the latest version. There will be constant change in this domain and it represents the most variable group of system components.

### Systems

The systems domain is broad as it encompasses any automated actor related to the solution. This includes Head-End systems acting as an intermediary between devices and other systems, the clients' back-office systems (monitoring, management, billing, etc.), and business partner systems. These do not change as much as the devices but do evolve significantly over the life of the system.

### Mediation

This tier is responsible for data marshaling (mediation) between each of the devices and systems with the unified data management.

The mediation domain abstracts the ever-changing device and system domains from the more stable core of the system. It is responsible for marshaling the many data models of the external hardware and software components to the unified model of the solution.

### Data Management

This is the collection of components responsible for the storage, retrieval, and integrity of the data at rest. Components in this domain are least likely to change over the life of the application. Solution components in this domain may only need to change yearly. A properly normalized data model and scaleable storage infrastructure can go years without change.

### Processing

When the client desires to use the data, components in the processing domain are involved. Analytics and Processing are where business logic is applied to the data to generate information.

The rate of change in this domain is relatively high between installations, but the change is usually in components of the processing domain. Processing components can be grouped to facilitate the separation of concerns and honor differing rates of change. The data validation processors will change at a lower rate than the analytics processors which are constantly changing to handle new use cases. Command and control processors change at differing rates and it is each of the processors in this domain is grouped based on their rates of change.

Additionally, delivery teams are created and assigned a mix of these processors to even out the workload and help coordinate release schedules. The few processors with the highest rate of change may be assigned to one team while all the remaining processors are the responsibility of another.

### Presentation

Components that involve the representation of data and information to humans exist in the presentation domain. This includes all manner of Human Machine Interface (HMI) components and any reporting components.

The rate of change is this domain is probably the highest of all others with the exception of the device domain. The user interface components will be updated regularly, with new visualizations and capabilities. New HMI components will be introduced as the product evolves.

### Rates of Change

The expected rates of change for our architecture are as follows from the fastest rate of change to the slowest:
1. Data Management
1. HMI (dashboards, etc.)
1. Device Mediation
1. Custom Processors
1. Analytics Processors
1. Core Processors
1. Data Model
1. Cloud Infrastructure

Data management and related components change constantly. Data must be received, verified, and stored for efficient retrieval. Data management operations have a regular need for changes and updates to the tools needed to keep data flowing.

User interfaces are changing daily. New views and dashboards are required based on the needs of each user in each customer.

Device mediation changes regularly. Devices need to be updated and maintained. Head-end systems need to be managed, monitored, updated, configured, and deployed regularly to keep up with growing needs.

Custom processors are needed by the clients, so fast delivery is critical. Expect weekly releases for custom processors.

Analytics processors are relatively standard, but still updated regularly as new research reveals advances in analytical models.

The core product (processors) will not change much. Maybe features and bug fixes are released every quarter or so.

The data model is relatively static as it has been normalized to support a variety of data types and processing needs. This layer may change only once a year.

The infrastructure on which all this runs is probably the most static of all layers. Although it regularly scales horizontally to accommodate additional customers and their data, the design and configuration of infrastructure do not need to change.

## Recommendations

Develop the tools, tooling, and mechanisms that instrument the rates of change you need. A good place to start is looking at the backlog. Another place to look is in your delivery stream. Track the number of pull requests and commits to discover frequently changing code.

Encapsulate the parts that vary so they don’t leak out/affect other areas. Do not be afraid to refactor. Start by establishing interfaces and abstractions and using the [Strangler pattern](https://en.wikipedia.org/wiki/Strangler_fig_pattern) to migrate new code to replace the old.

Refactoring to reduce team dependencies. Decompose complex components into smaller, easier-to-manage projects. Assign responsibility for those components to teams with similar rates of change or regular dependencies on that project.

This may mean that if you have highly changing software, you architect ways that drive this change via mechanisms that are “easier” to change than others.

Engineers tend to work bottom-up in decision processes and this normally leads to monolithic systems with few layers. Look at the system as a whole and not from a limited perspective.

Systems with fewer dynamic layers are usually more costly to change but yield higher returns in collaboration and reuse. If you think improved collaboration will reduce delivery times, you should investigate the reasons for the collaboration. Consider making one team responsible for multiple parts of the system.

Consider structuring teams based on rates of change. Teams responsible for components with high rates of change should not be responsible for too much of the system. Front-end developers usually have high rates of change and should not also be responsible for other parts of the system. Back-end systems traditionally have lower rates of change and back-end teams can usually be responsible for many more components without adversely affecting their throughput.

Look for components that can be decomposed into smaller units. Monolithic services take longer to maintain and evolve than several smaller services.

## Summary

Far too many systems are a "Big Ball of Mud" [[2](#2)] that results in a simple change to require a change to multiple parts of the system. Adding a feature or addressing a defect results in changes to multple components of the system. Simple changes require coordination across multiple teams and places stress on each teams release scheduling. 

This can be avoided by designing your system to group components with similar rates of change together to isolate change in the system and make evolving and maintaining the system easier.


## References
<ol>
  <li id="1">Stewart Brand, How Buildings Learn, Adaptive Architecture in a Changing World, Viking, 1994</li>
  <li id="2">Brian Foote and Joseph Yoder, Big Ball of Mud, June 1999; Accessed <a href="http://laputan.org/mud/mud.html#ShearingLayers">Online</a></li>
</ol>