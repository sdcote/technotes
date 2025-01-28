---
title: Qualities
description: >-
  Architecture is the structure and behavior of a system designed to intentionally 
  achieve certain externally visible qualities. This section covers those qualities.
weight: 2
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

Qualities describe a system's behavior, not what it is expected to do. They are a formal definition of the system's non-functional requirements.

There are four classes of system qualities.
1.	**Runtime** - qualities that can be observed and measured as the system executes.
1.	**Non-runtime** - cannot be observed and measured through system execution.
1.	**Business** - required by the business environment or the market.
1.	**Architecture** - directly related to the architecture itself.

## Importance

The definition of system qualities is vital for several reasons:
- **Quality Assurance**: System qualities help ensure the system meets specific quality standards, such as performance targets, security measures, and usability criteria.
- **User Experience**: System qualities can significantly impact the overall user experience. For example, response time and reliability can dramatically affect how users perceive the system.
- **System Performance**: System qualities help define the system's performance characteristics, such as scalability, availability, and response time. These qualities ensure the system can handle the expected workload and perform efficiently.
- **Compliance and Security**: System qualities related to security, compliance with regulations, and data privacy are essential for protecting sensitive information and ensuring legal compliance.

## Decision Criteria

Establishing clear decision criteria is essential before making any design decisions. Without such criteria, the resulting design choices will likely produce inconsistent outcomes. 

Critical decision criteria involve identifying the desired qualities the system must exhibit. For example, should the system prioritize speed, security, or scalability? Should it be easy to maintain, upgrade, or integrate with other systems? 

All required system qualities must be explicitly documented so decision-makers can use them to evaluate design alternatives. This list is often included in the design deliverables and documentation introduction section.

Additionally, the list of desired qualities should be prioritized. In many cases, different design alternatives will exhibit the same attributes but at the expense of others. This trade-off is often likened to the traditional "Iron Triangle" of budget, schedule, and scope. For instance, a design alternative might meet schedule and scope requirements, but if the overarching goal is to create an affordable system, that option may not be viable. Some projects operate under large budgets but have extremely tight schedules. In such cases, a design alternative that prioritizes schedule adherence might be the optimal choice, even at a higher cost. 

A prioritized list of system qualities offers a structured framework for making precise and deliberate design decisions. Without such a list, decisions risk becoming arbitrary, ultimately leading to project failure.

### Criteria for Architecture Selection
Quality depends on architectural choices. Technical design decisions that affect externally observable qualities are architectural decisions.

Architecture can only permit, not guarantee, any quality  attribute: 

> What the architecture gives, the implementation can take away.

The system can be architected to be secure, but implementing the design can leave it vulnerable to attack. For example, the architecture specified 140-2 encryption, but the implementation exposed the master passwords and private keys in a text file.

### Architectural Tactics
Architectural tactics outline strategies for meeting specific quality requirements. Architects possess a broad array of tactics for each quality aspect. The architect selects the most appropriate tactic based on the system's needs and the operating environment. 

For example, performance tactics may include enhancing processing algorithms, implementing parallel processing systems, or adjusting event scheduling policies. No matter which tactic is chosen, it is crucial to provide justification and document the decision-making process.

### Quantifiable Qualities
Qualities are not always measurable and are often subjective. As a result, design decisions are typically made to enhance or diminish a quality rather than to achieve a specific, quantifiable value.

While quantifiable qualities are ideal, they are not always feasible to define, or their measurement may be challenging to determine. For instance, system usability might be difficult to quantify directly, but the volume of help desk tickets could indirectly indicate usability. Similarly, a system's performance might be evaluated based on metrics such as the number of transactions completed within a given time frame.

In such cases, quality scenarios can be valuable tools for making qualities more measurable and actionable.

### Quality Scenarios
Quality attributes need to be described in specific scenarios to provide a clear understanding of how the system should perform. For example, a scenario could be: "When 100 users initiate the 'complete payment' transition, the payment component should process the requests within an average latency of three seconds under normal circumstances." This scenario helps architects make quantifiable arguments about the system by defining the source of stimulus (users), the actual stimulus (initiate transaction), the affected artifact (payment component), the environment (regular operation), the effect of the action (transaction processed), and the response measure (within three seconds).

Creating such detailed scenarios requires identifying relevant requirements and proposing component ideas. Although writing practical scenarios may take time, it is a crucial skill as it translates vague software behaviors into measurable goals. These quantifiable goals guide the selection of architectural approaches and tactics during system design.

## Example

The following is the prioritized list of qualities to guide all technical decisions for a $1.6M project to replace HP Service Center with ServiceNow. The "Decision Framework" was included in all deliverables to reinforce the system qualities the stakeholders determined to be critical to project success.

#### Decision Framework

Stakeholders have agreed to leverage “out of the box” ServiceNow features for Process Capability uplift (configuring as needed and avoiding customization); participants also agreed to the following decision-making priorities to guide planning and execution:


| Priority | Quality | Description/Notes |
| ---- | ------------ | ------------------------------------------------------------ |
| 1    | User Experience | Ensure a quality user experience. Defects do not hinder IT Run Capability efficiency and capability uplift. Secure the data and application access. |
| 2    | Scope        | The scope is defined as implementing the ServiceNow Service Automation Suite and associated data cleanup and systems integration to enable the replacement of HP Service Center. |
| 3    | Cost         | The project must meet the established budget. If necessary, additional funds will be requested through change control to realize the value, quality, and scope objectives. |
| 4    | Schedule     | Schedule considerations: Ensure sufficient time to incorporate change management, business value, and quality goals while minimizing the time frame to decommission the HP Service Center (hold down “bubble cost”). |
| 5    | Value        | The completed project satisfies the business goals and objectives stated in the business case. |
| 6    | Architecture | The ServiceNow SaaS solution and underlying architecture were vetted in the software evaluation. Leverage SaaS to reduce the cost and complexity of future software upgrades. Meeting NFRs is vital to avoiding impacts on IT Run Capability, for example, IT Service Team productivity. Improve integration of interfacing systems. The architecture is already set. The ability to change is limited. |

## References

<ol>
  <li id="1">http://www.softwarearchitectures.com/qa.html</li>
</ol>
