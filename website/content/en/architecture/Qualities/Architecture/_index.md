---
title: Architecture Qualities
description: There are qualities directly related to the architecture itself that are important to achieve. These include the conceptual integrity of the system, architectural correctness and completeness, and buildability.
weight: 5
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

- **Conceptual Integrity** - The architecture does similar things in similar ways.
- **Correctness/Completeness** - Meeting all the systems requirements and runtime constraints.
- **Buildability** - Ability of the system to be completed with available resources.

## Conceptual Integrity

Conceptual Integrity is the underlying theme or vision that unifies the system's design at all levels. The architecture should do similar things in similar ways.

Fred Brooks writes that conceptual integrity is the most important aspect of a system:  
> Conceptual integrity is central to product quality. Having a system architect is the most important single step toward conceptual integrity.  [[1](#1)]

Conceptual integrity is typically achieved using either a single architect or a small, well-coordinated architecture team.  Brooks insists that having a separate architect is critical for a team approach, even on teams as small as four people.

## Correctness / Completeness

Correctness and completeness mean that an architecture should allow for the satisfaction of all requirements.  These qualities are essential for the architecture to allow for the meeting of all behavioral and quality requirements and runtime resource constraints.

## Buildability

Buildability is the quality of the architecture that allows the system to be completed by the available team in a timely manner with available resources, and to be open to certain changes as the system development progresses.  Buildability is the ease of constructing a desired system.  It is usually measured in terms of cost and time.  Thus, there is a relationship between the buildability quality and various cost models.  However, buildability is usually more complex that what is usually covered in the cost models.  

A system is created from certain materials, and these materials are composed using a variety of tools.  So one element of buildability is the match between the materials that are to be used in the system and the tools that are available to manipulate these materials.  Another aspect of buildability is the state of knowledge about the problem to be solved.  Thus, a design that casts a solution in terms of well-understood concepts is more buildable than a design that introduces new concepts.

## References
<ol>
  <li id="1">F. P. Brooks, Jr., The Mythical Man Month, Reading, MA, Addison Wesley, 1975</li>
</ol>