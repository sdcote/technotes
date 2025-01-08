---
title: Architecture Artifacts
description: Don't waste time generating marginally useful documnetation. Focus on documentation that is the most valuable and contributes to the success of your projects.
weight: 3

---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

## Documentation May Be Worthless, but Documenting is Priceless

The best way to begin to understand the entirety of your context is to perform the research to document it. 

Documents are all about communication. It helps convey a common understanding. There is a secondary benefit of documentation; the very act of generating the documentation often leads to discovery.

Once you document your understanding of something and socialize it, new insights are revealed through the process of research and the correction of others.

Once you socialize the model, you will often find others will correct you and you will discover what the existing system owners did not know.

In almost every project, the inquiry required to generate a document unveils some detail or fact not known by primary decision-makers. Maybe assumptions were made or the environment has changed since the last time the environment was investigated, but it is a rare event to research a system or process and not find something new for those responsible for the system.

So while the documentation may to become obsolete over time and require constant maintenance, the act of maintaining the record causes regular inquiry as to the state of the system and its current business context. It is this regular monitoring of the systems state that keeps systems relevant, and identifies when they are no longer needed or require refactoring to provide value to the organization.

## Dealing with Change

Maintaining documentation is costly and it often does not provide sufficient returns to justify keeping it absolutely current. Since much of the value is in the act of documenting, it is often better to re-visit documentation at the onset of major revisions or upgrades.

Business Requirements can change weekly. Architecture documents normally do not deal with such dynamic change, but it can happen. The architecture team should always be watchful for uncertainty in their problem domain which can invalidate strategic decisions. The need to be brought to the attention of stakeholders so decisions can be made as to the effects of change on strategic technical decisions.

As is general practice, try to isolate the change in a separate problem domain to keep the core of the solution stable and allow the edges to be pliable. 

## Documentation Aids Communication

Pictures convey more information than words.

Simple diagrams are easier to consume.

Use a consistent style across all teams.

Documentation does not replace conversation.

The amount of documentation is not a valid performance metric.


## Architectural Views

An architectural view is a simplified description (an abstraction) of a system from a particular perspective or vantage point, covering particular concerns, and omitting entities that are not relevant to this perspective

Architectural views = slices through models


## Important Artifacts
1. Quality Attribute List
1. System Context
1. Integration Catalog
1. Decision Log
1. Component Model
1. Sequence Diagrams
1. Deployment Model
1. Failure Mode Effect Analysis


## Non Functional Requirements

Architecture normally relies on strategic non-functional requirements. Logging strategies are important to observability.

There are few architectural decisions related to documentation, but a unified documentation approach can save time and improve maintainability in the long run.


## Unified Modeling Language

It is a common language to describe architecture.

It has been around for decades, mostly unchanged.

It’s simple – really!

Use only what you need.

### XMI – XML representations of UML

Standard interchange format between UML tools.

It is relatively easy to generate UML models programmatically.
