---
title: Agile Architecture
description: >-
     Architecture does not require waterfall methodologies or big up front (BUF) 
     design. Architecture decisions can be made as late as possible.
weight: 200
---

{{< alert color="warning" title="Work In Progress" >}}This page contains fundamental truths relating to systems design and where the concept of architecture relates to that process. This page needs to be formatted into a logical unit.{{< /alert >}}

We have said before that architecture is not BUFD. That is a myth amplified by the wide adoption of agile practices and the related distrust of waterfall design.

Agile is an Emergent Design, Right?

> The best architectures, requirements, and designs emerge from self-organizing teams.
— Agile Manifesto

**emergent design** —the evolutionary process of discovering and extending the design only as necessary to implement and validate the next increment of functionality.

The problem we run into is one of Context. The team is best suited to determine its own design, but it seldom has visibility into the needs or the state of systems outside the team's sphere of influence. Your asset management runs perfectly, it is a shame nobody else in the enterprise can use it integrate with it, or correlate business analytics from it…

Sometimes the Product Owner does not know to ask for more big-picture capabilities…Product Owners are often not inclined/incented to be aligned with everyone else in the enterprise.

## Who Needs Formal Architecture?

**Won’t the architecture emerge from natural development?**

Yes, but the architecture only takes into account the scope of the development team. The resulting architecture may be vastly different from the rest of the systems leading to increased operation and maintenance costs.

**Isn’t the team best prepared to make decisions enabling the next increment of functionality?**

Yes, but only for the context of their project or “sphere of influence”.

**Isn’t architecture the structure of the system at the end of each iteration?**

Yes, but the architecture only takes into account the scope of the completed iterations. (If you don't know where you are going you might not like where you end up.)

## Scaling

There comes a point at which emergent design is an insufficient response to the complexity of larger-scale system development.

Teams cannot anticipate changes that occur outside their environment.

Teams do not have the time or opportunity to understand the entire system or every deployed solution.

Different teams will evolve differently.

A software company with one development team offering one product is different from a company offering many different products or a company utilizing multiple teams.

Product marketing strategies determine which system qualities become product differentiators.

Mergers & acquisitions result in multiple teams working on multiple products often in geographically disparate locations.

Companies that offer customer solutions normally involve the products of multiple teams.

Management desires to use outsourced development to reduce annual headcount costs.

When a development team does not have visibility into other development teams, product strategies, market positioning, corporate goals, and strategies, it can make architectural decisions that are misaligned with the direction of the rest of the company.

**Quite simply, agile teams need a mechanism to coordinate their decisions with other teams in the organization.**

Other implementation teams, 

Product Marketing / Sales,

Business Partners, Executive Leadership,

etc…



## Intentional Design

Collaboration on a set of purposeful, planned architectural initiatives to enhance:
- Solution design,
- Inter-team design,
- Implementation     synchronization,
- Consistency between product offerings,
- Alignment with corporate goals and objectives,
- System Qualities (and NFR.)

 

Developing a set of strategies with align with corporate objectives and goals which help guide implementation teams along an intentional direction in coordination with the rest of the organization.

Architecture is a part of intentional design. It is a strategic approach to delivering products with is shared by the entire delivery chain. 

## Architecture Allows Agile to Scale

Developing strategies allows multiple teams to develop in parallel while reducing integration and interoperability risks.

We are talking about just enough System Architecture or Product Architecture to enable development activities to occur in a coordinated fashion.

This is not Big Up Front Design (BUFD) or defining everything at the onset; we are talking about just enough design to ensure the next iteration occurs in a coordinated fashion.

The goal is for the products of each team to integrate well at the then of their sprints.


## Collaboration is Key

The challenge for agile teams in larger projects is to achieve the proper balance of emergent and intentional design.

The key is collaboration on strategic delivery approaches:
1. Initial architecture constrains product development,
2. Design emerges,
3. The agile team provides feedback on intentional design,
4. Architecture evolves.

Architecture is a collaboration.

## Architecture Guidance

Architects are available to team leaders to clarify technical approaches' alignment.

Architects are available to attend team meetings and sprint planning.

Architects collect feedback from development and operations.

Architects work with the Product Owner to:
- Coordinate Release Plans,
- Coordinate and Clarify Technical Approaches,
- Develop Capability Model and Road Map…

Share the results of Architectural Spikes with all teams and stakeholders.

## Agile Architecture Values

- Balanced Design
- Testable Qualities
- Being Hands-on: coding, designing, reading/reviewing code, prototypes, demos…
- Sustainable Development
- Fast Value Delivery
- Risk Reduction
- Architecture Refinement

Don’t over-design but don’t under-architect.

Respect your system’s shearing layers. Understand the rates of what changes. Isolate rapidly changing parts/components from more stable ones.

Make what is too difficult, time-consuming, or tedious easier. Create tools, leverage design patterns, build or use frameworks, use data to drive behavior…

Architect for sustainable development/delivery of features and customer value.

Refine your architecture

## Pragmatic Architecture

Just enough architecture to achieve goals and enable coordination.

Generate only the artifacts that provide value to teams.

Model the big picture and communicate global needs to teams.

Allow teams to innovate without going “off the ranch.”

Assist teams in implementing strategic approaches (yes, coding).

Perform Architecture Spikes to evaluate approaches.

Demonstrate the results of Architecture Spikes to everyone.

Be available to engineering and management.

## Architecture Owner

When a full-time architect is not necessary.
- Similar to the Product Owner.
- Could be a role within the team.

Decision Maker.
- When collaboration leads to a deadlock, the owner makes the decision.
- Responsible for keeping models current and visible.

Differs from the traditional “Architect.”
- Is not the sole decision maker: more of a “tie-breaker.”
- Facilitates collaboration amongst the team.

## A Couple of Thoughts About Team Ownership

Sometimes people don't agree.

It doesn't scale. 

The problem with team ownership is this: Sometimes people don't agree. This strategy can fall apart dramatically when the team doesn't come to an agreement, hence you need someone in an architecture owner role to facilitate agreement. In one agile team, this is often a lead developer.

It doesn't scale. When your team is large or geographically distributed, two of the eight scaling factors called out in the Agile Scaling Model (ASM), you will organize your team into a team of sub-teams. Architecture at scale requires a coordinating body in such situations.

## When Architecture is Good Enough

- Defects are localized
- Stable interfaces
- Consistency
- Developers can easily add new functionality
- New functionality doesn’t “break” existing architecture
- Few areas that developers avoid because they are too difficult to work with
- Able to incrementally integrate new functionality
