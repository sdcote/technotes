---
title: Non-Runtime Qualities
description: There are qualities that cannot be observed and measured through system execution.
weight: 2
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

- Testability - Ease of making a system reveal its faults through testing.
- Modifiability (Variability) - Ability to make changes quickly and cost effectively.
- Portability - The ability to operate on different computing environments.
- Reusability - Components can be used again in future applications.
- Integrability - Ability of separately developed components to work together.

Integrability is the ability to make the separately developed components of the system work correctly together. This in turn depends on the external complexity of the components, their interaction mechanisms and protocols, and the degree to which responsibilities have been cleanly partitioned, all architecture-level issues. 

Modifiability, in all its forms, may be the quality attribute most closely aligned to the architecture of a system. The ability to make changes quickly and cost effectively follows directly from the architecture: Modifiability is largely a function of the locality of any change. Making a widespread change to the system is more costly than making a change to a single component, all other things being equal. There are exceptions, of course. 

Portability is the ability of a system to run under different computing environments. These environments can be hardware, software, or a combination of the two. A system is portable to the extent that all of the assumptions about any particular computing environment are confined to one component (or at worst, a small number of easily changed components).

Reusability is usually taken to mean designing a system so that the system’s structure or some of its components can be reused again in future applications. Designing for reusability means that the system has been structured so that its components can be chosen from previously built products; reusing components reduces the time to market and costs of building and implementing future systems.

Testability refers to the ease with which software can be made to demonstrate its faults through (typically execution-based) testing. In particular, testability refers to the probability that, assuming that the software does have at least one fault, the software will fail on its next test execution. For a system to be properly testable, it must be possible to control each component’s internal state and inputs, and then to observe its outputs.




