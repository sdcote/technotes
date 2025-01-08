---
title: Architecture and Design
description: Relationship Between Architecture and Design
weight: 7
---

{{< alert color="warning" title="Work In Progress" >}}This page contains fundamental truths relating to systems design and where the concept of architecture relates to that process. This page needs to be formatted into a logical unit.{{< /alert >}}



Architectural decisions are the most fundamental of decisions; changing them will have significant ripple effects. 



Every interesting software-intensive system has an architecture



The most successful software architectures are intentional, manifest, and visible 



Architecture is design, but not all design is architecture.

- Design that affects an externally visible property is Architecture
- Strategic Architecture versus Tactical Architecture

There is no clear boundary line. - One person’s architecture may be another person’s implementation and vice versa.



Developers make architectural decisions.

- Modules
- Adapters
- Plug-Ins



The architectural view of a system is an abstract view that distills away the details of implementation, algorithm, and data representation and concentrates on the behavior and interaction of “black-box” components.

Architecture establishes the context for design and implementation 

Think of Architecture as a shell containing the design containing the implementation. The code is contained within the implementation.



Software architecture is the first step of designing a system. 

Software architecture is a “First Cut” at solving the problem and designing the system.

Architecture is design, but not all design is architecture. That is, many design decisions are left unbound by the architecture and are happily left to the discretion and good judgment of downstream designers and implementers.

Remember our definition of software architecture (from Software Architecture in Practice, 2nd edition): 

“...the structure or structures of the system, each of which comprises elements, the externally visible properties of those elements, and the relationships among them.” 

Thus, if a property of an architectural element is not externally visible, or discernible, to any other architectural element, that element is not architectural. The selection of a data structure, along with the algorithms to manage and access that data structure, is a typical example.

The reason an architect does not make a component part of the architecture is that its existence or nonexistence was not material to the overall goals of the architecture. 

Strategic Architecture is what normally applies to the Business/Stakeholder Needs

Tactical Architecture is what normally applies to the problem domain or solution context

No Clear Boundary Line No scale or scope or measure or line divides what is architectural and what is not. One person’s architecture may be another person’s implementation and vice versa.

The architect draws the boundary between architectural and non-architectural design by making those decisions that need to be bound for the system to meet its development, behavioral, and quality goals.

## Developers Make Architectural Decisions 

Tactical Architecture decisions are made regularly, often within the context of the Problem Domain.
