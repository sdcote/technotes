---
title: Qualities
description: Architecture is the structure and behavior of a system in such a manner as to intentionally achieve certain externally visible qualities. This section covers those qualities
weight: 2
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

Qualities are not the same as requirements although qualities can be required. i.e., a requirement is to have a quality of high availability.

Qualities describe how a system is to behave, not what it is expected to do.

They are a formal definition of the non-functional requirements of the system.

System qualities must be prioritized otherwise it may be difficult to perform a trafe-off analysis

The definition of system qualities is important for several reasons:
- **Quality Assurance**: System qualities help ensure that the system meets specific quality standards, such as performance targets, security measures, and usability criteria.
- **User Experience**: System qualities can greatly impact the overall user experience of a system. For example, qualities related to response time and reliability can significantly affect how users perceive the system.
- **System Performance**: System qualities help define the performance characteristics of the system, such as scalability, availability, and response time. These qualties are crucial for ensuring that the system can handle the expected workload and perform efficiently.
- **Compliance and Security**: System qualities related to security, compliance with regulations, and data privacy are essential for protecting sensitive information and ensuring legal compliance.

Qualities are not always measurable and are often subjective. Architectural decisions are therefore made with the intent to strengthen or weaken a quality rather than to achieve a discrete, measurable value.

It is best to have quantifiable qualities.

Criteria for Architecture Selection
Quality is Dependent on Architectural Decisions
- Not all aspects of all qualities are affected by architecture
- Architecture can only permit, not guarantee, any quality  attribute:
    - "What the architecture gives, the implementation can take away."

We define the term quality here as the fitness of a product for its intended use:  How well does the product do what it was designed to do?

There are four classes of system qualities.
1.	Runtime
1.	Non-runtime
1.	Business
1.	Architecture

### Architectural Tactics
Architectural tactics outline the strategies for achieving a specific quality requirement. Architects have a wide range of tactics to choose from for each quality aspect. It is the architect's responsibility to carefully select the most suitable tactic based on the system's requirements and the operating environment.

For instance, performance tactics could involve improving processing algorithms, implementing parallel processing systems, or adjusting event scheduling policies. Regardless of the tactic chosen, it is essential to provide justification and document the decision-making process.

### Quality Scenarios
Quality attributes need to be described in specific scenarios to provide a clear understanding of how the system should perform. For example, a scenario could be: "When 100 users initiate the 'complete payment' transition, the payment component should process the requests within an average latency of three seconds under normal circumstances." This scenario helps architects make quantifiable arguments about the system by defining the source of stimulus (users), the actual stimulus (initiate transaction), the affected artifact (payment component), the environment (normal operation), the effect of the action (transaction processed), and the response measure (within three seconds).

Creating such detailed scenarios requires identifying relevant requirements and proposing component ideas. Although writing effective scenarios may take time to master, it is a crucial skill as it translates vague software behaviors into measurable goals. These measurable goals guide the selection of architectural approaches and tactics during system design.

## References
<ol>
  <li id="1">http://www.softwarearchitectures.com/qa.html</li>
</ol>
