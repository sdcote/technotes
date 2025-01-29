---
title: Non-Runtime Qualities
description: There are qualities that cannot be observed and measured through system execution.
weight: 3
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

- **Testability** - Ease of making a system reveal its faults through testing.
- **Modifiability** (Variability) - Ability to make changes quickly and cost-effectively.
- **Portability** - The ability to operate in different computing environments.
- **Reusability** - Components can be used again in future applications.
- **Integrability** - Ability of separately developed components to work together.

## Integrability 

Integrability is the ability to make the separately developed components of the system work correctly together. This, in turn, depends on the external complexity of the components, their interaction mechanisms and protocols, and the degree to which responsibilities have been cleanly partitioned, all of which are architecture-level issues. 

## Modifiability

Modifiability, in all its forms, may be the quality attribute most closely aligned to a system's architecture. The ability to make changes quickly and cost-effectively follows directly from the architecture: Modifiability is largely a function of the locality of any change. Making a widespread change to the system is more costly than making a change to a single component, all other things being equal. There are exceptions, of course. 

## Portability

Portability is the ability of a system to run under different computing environments. These environments can be hardware, software, or a combination. A system is portable to the extent that all assumptions about any particular computing environment are confined to one component (or, at worst, a small number of easily changed components).

## Reusability

Reusability is usually understood to mean designing a system so that its structure or some of its components can be reused again in future applications. Designing for reusability means structuring the system so that its components can be chosen from previously built products; reusing components reduces the time to market and costs of building and implementing future systems.

## Testability

Testability refers to the ease with which software can demonstrate faults through (typically execution-based) testing. In particular, testability refers to the probability that, assuming the software has at least one fault, it will fail on its subsequent test execution. For a system to be correctly testable, it must be possible to control each component’s internal state and inputs and then to observe its outputs.



