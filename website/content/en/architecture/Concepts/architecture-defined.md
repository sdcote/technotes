---
title: Architecture Defined
description: Searching for a common definition of architecture.
weight: 1
---

## What is Architecture

There are many definitions of what the architecture of a technical system is. Most are based on a specific perspective limited to facets of a system such as software, hardware, or data. From all generally accepted definitions, there are common elements shared by all. At the highest level:

> Architecture is an intentional plan to achieve specific qualities in a system. It is all the components of a system and their relationships deliberately organized to achieve externally observable characteristics.

What this means is strategic design decisions are made with the goal of creating a system that exhibits a set of desired characteristics.

### The IEEE Definition

The IEEE has a good definition of a systems architecture that is oft-cited in many papers:

> Architecture is the fundamental organization of a system embodied in its components, their relationships to each other, and to the environment, and the principles guiding its design and evolution. [[1](#1)]

### The ISO/IEC Definition

The ISO/IEC 42010:2011 definition of architecture is similar to the IEE definition in its breadth:

> "The fundamental organization of a system, embodied in its components, their relationships to each other and the environment, and the principles governing its design and evolution."  [[5](#5)]

This definition is technically identical to ANSI/IEEE Std 1471-2000.

### TOGAF Definition

In The Open Group Architecture Framework (TOGAF), “architecture” has two meanings depending on the context: 

>A formal description of a system, or a detailed plan of the system at a component level to guide its implementation [[6](#6)]

> The structure of components, their inter-relationships, and the principles and guidelines governing their design and evolution over time [[6](#6)]

The architecture can be the documented specification or the design described in that specification.

### Software Architecture
Carnegie Mellon University Software Engineering Institute has a well-accepted definition of software architecture:

> The software architecture of a program or computing system is the structure or structures of the system, which comprise software elements, the externally visible properties of those elements, and the relationships among them.  [[2](#2)]

Several well-known software architects, a few of whom signed the Agile Manifesto, derived and refined a definition of software architecture based on work by Mary Shaw and David Garlan (Shaw and Garlan 1996). Philippe Kruchten, Grady Booch, Kurt Bittner, and Rich Reitman have presented this definition of software architecture:

> Software architecture encompasses the set of significant decisions about the organization of a software system including the selection of the structural elements and their interfaces by which the system is composed; behavior as specified in collaboration among those elements; composition of these structural and behavioral elements into larger subsystems; and an architectural style that guides this organization. Software architecture also involves functionality, usability, resilience, performance, reuse, comprehensibility, economic and technology constraints, tradeoffs, and aesthetic concerns.  [[3](#3)] [[4](#4)]

### Common Elements
All these definitions have some common elements:

- Architecture defines major **components**,
- Architecture defines component **relationships** (structures) and **interactions**,
- Architecture omits content information about components that do not pertain to their interactions,
- The behavior of components is a part of architecture insofar as it can be discerned from the point of view of another component,
- Every system has an architecture (even a system composed of one component),
- Architecture defines the rationale behind the components and the structure,
- Architecture definitions do not define what a component is,
- Architecture is not a single structure -- no single structure is the architecture.

### A Pragmatic Definition

Taking all the generally accepted definitions together, it becomes clear that architecture is:

- Part of the design process,
- Concerns the structure of systems along with their behavior and relationships,
- Is a strategy for meeting requirements,
- Influenced by technical, business, and social factors,
- Subjective - there is no single "right" answer.

Regardless of the perspective, a more pragmatic definition of architecture is:

***Architecture is the strategic design and related activities that affect a system's externally observable qualities and provide guidance to tactical design decisions.***

This general definition combines salient elements from the other generally accepted definitions and 


## References
<ol>
<li id="1">ANSI/IEEE Std 1471-2000, Recommended Practice for Architectural Description of Software-Intensive Systems.</li>
<li id="2">Bass; Clements; Kazman; Software Architecture in Practice, 2ND Edition, Reading, MA: Addison-Wesley, 2003</li>
<li id="3">Philippe Kruchten;  <a href="https://philippe.kruchten.com/wp-content/uploads/2009/07/kruchten-090608-agile-architecture-usc.pdf">Software Architecture and Agile Software Development —An Oxymoron?</a></li>
<li id="4">Grady Booch; <a href="https://www.ict.griffith.edu.au/teaching/2501ICT/pdf/Arch.pdf">Software Architecture and the UML</a></li>
<li id="5">ISO/IEC 42010:2007, Systems and Software Engineering – Recommended Practice for Architectural Description of Software-Intensive Systems, Edition 1.</li>
<li id="6">The Open Group. (2018); <a href="https://pubs.opengroup.org/architecture/togaf9-doc/arch/">The TOGAF® Standard, Version 9.2</a></li>

</ol>

