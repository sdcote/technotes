---
title: Shearing Layers
description: Different parts of a system are more dynamic than others. By grouping together the parts of your system that change at the same rates, your system becomes much easier to maintain.
weight: 4
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

Complex systems tend to have areas with differing rates of change. A house, for example, sits on a lot that rarely changes. The foundation on the lot might chage if there are additions to the house but the lot does not change. The walls of the house might change if there are addition, but they are relatively static. The services of the house (electrical, plumbing, HVAC, etc) change more often than the structure. The paint on the wall change more ofthen that the walls. The furniture in the house change more often than the paint. Understanding these shering layers helps with development and maintenance.  [[1](#1)]

To ensure stability in the solution, it is advisable to group together elements that change at similar rates. Changes should be localized to specific parts of the system without necessitating modifications across the entire system.

For instance, when a web page requires modifications, it is more efficient for a Web Developer to only update a CSS or HTML file without needing to alter server code. The server code should remain unaffected by changes to UI elements on a page, as the page is subject to frequent modifications while the server is not. This separation creates a shearing layer between the UI page and the server. While the data itself undergoes continuous changes, the data model remains relatively constant, with a shearing layer between the data and its model.

Organizing components based on shearing layers not only helps limit changes to specific domains but also facilitates project management and development. Teams can be scaled up or down based on the pace of change, with some teams expanding to support rapid changes while others remain small and agile. For instance, a project may have a large team of web developers but only a small team of database administrators.

Yoder and Foote’s Software Shearing Layers
> Factor your system so that artifacts that change at similar rates are together.
> —Foote & Yoder, Ball of Mud Pattern [[2](#2)]

## Separation Of Concerns
This which do like processing can be grouped together

This allows teams with the proper skill set to be focused on a part of the system. Web Developers can work one part of the solution while Database Administrators and Network engineers can work on their respective areas.

## Shearing Layers
This which change at similar rates should be grouped together to provide stability to the solution. Changing should be limited to just a portion of the system and not require systemic modifications.

For example, everytime a web page needs to change, it would be more efficient if a Web Developer only changed a CSS or HTML file and not have to change server code. The server code should not have to change just because a UI element is being added to a page. The page is prone to regular change but the server not. There is a shearing layer between the UI page and the server. While the data itself is a stream of change, the data model is relatively constant in nature; there is a shearing layer between data and its model.

It is a good practice to separate your components by shearing layers so you can limit change to a single domain and not have to disturb multiple components to make changes to the system.

Decomposing the system based on shearing layers has the added benefit of helping manage the installation and development of the project. Some teams may be increased in size to support the rate of change while others can remain small and agile. It is not uncommon for there to be an army of web developers but only a small team of database administrators on a project.

Develop the tools, tooling, and mechanisms that instrument the rates of change you need. 

Encapsulate the parts that do vary so that they don’t leak out/affect other areas. 

This may mean that if you have highly changing software, you architect ways that drive this change via mechanisms that are “easier” to change than others

—data driven techniques, meta techniques, whatever…. 

BTW, engineers tend to work bottom-up in decision processes while architects tend to work top-down…but that is a whole discussion in itself

### Respect your Shearing Layers

Architecture decisions with less dynamic layers are usually more costly to change but yield higher returns in collaboration and reuse.

## Case Study

Let's look at our case study. Data is acquired from devices in the field. While it is possible to communicate with the device directly, many(most) devices will communicate with a Front-End Processor (FEP) usually known as a "Head-End". Each vendor will offer a solution to connect their hardware with the customers system. Some solution providers have their own generic head-end to talk with other devices.

### Devices

While devices themselves don’t change (with regards to firmware capabilities) the number and versions will. 20k devices may support one version of the protocol and the next 30k devices may support the latest version. There will be constant change in this domain and it represents the most variable group of system components.

### Systems

The Systems domain is very broad as it encompasses any automated actor related to the solution. This includes Head-End systems acting as an intermediary between devices and other systems, the clients back-office systems (monitoring, management, billing, etc.) and business partner systems. These do not change as much as the devices, but do evolve significantly over the life of the system.

### Mediation

This tier is responsible for data marshaling (mediation) between each of the devices and systems with the unified data management.

The mediation domain abstracts the ever-changing device and system domains from the more stable core of the system. It is responsible for marshaling the many data models of the external hardware and software components to the unified model of the solution.

### Data Management

This is the collection of components responsible for storage, retrieval and integrity of the data at rest.

### Processing

When the client desires to use the data, components in the processing domain are involved. Analytics and Processing are where business logic is applied to the data to generate information.

The rate of change in this domain is relatively high between installations, but

### Presentation

Components which involve the representation of data and information to humans exist in the presentation domain. This includes all manner of Human Machine Interface (HMI) components and any reporting components.

The rate of change is this domain is probably the highest of all others with the exception of the device domain. The user interface components will be updated regularly, with new visualizations and capabilities. New HMI components will be introduced as the product evolves 


## References
<ol>
  <li id="1">Stewart Brand, How Buildings Learn, Adaptive Architecture in a Changing World, Viking, 1994</li>
  <li id="2">Brian Foote and Joseph Yoder, Big Ball of Mud, June 1999; Accessed <a href="http://laputan.org/mud/mud.html#ShearingLayers">Online</a></li>
</ol>