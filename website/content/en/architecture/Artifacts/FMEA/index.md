---
title: Failure Mode Effect Analysis
description: >
    As the design of the system evolves, regular and iterative analysis of 
    failure modes in their effects on the system is performed to predict and 
    address risk early in the life of the system.
weight: 8
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---

This is how we improve the reliability of complex systems through a simple process of identifying failure modes.

We all want reliable systems, even if they are not on our prioritized list of system qualities. We want our systems to exhibit:

- **Availability** - always ready to perform its function
- **Integrity** - contain correct, uncorrupted data
- **Functional Assurance** - behaving the way it is supposed to behave
- **Notification** of abnormal operations (e.g. failures)

## Reliability
When we talk about product reliability, the discussion tends to be centered around the quality which measures the probability that the product or device “will work.” A more formal definition of product reliability is:

Product reliability is the ability of a unit to perform a required function under stated conditions for a stated period of time.

The most common approach to ensuring reliability, particularly in agile methodologies, is to observe the system, (preferably under test scenarios and not in production), note the failures as they occur and address them reactively. This continues for the life of the system. It is common practice to repeatedly test systems to make them reveal their faults, but there are problems with this practice.

- Testing is expected to reveal all types of failures, but they don't. The development team does not have the time nor the knowledge to envision every possible scenario and created tests for them.

- As the system matures, costs of fixing discovered failures increase. It is much more cost-efficient to identify and address problems early in the process, preferably at design time.

### Quantitative Reliability
What is needed is a proactive approach to determining the probability of failures with a system before a faulty product is created. This allows the failures to be addressed before any code is written and potentially wasted.

This brings us to the concept of Quantitative Reliability:

Quantitative reliability is the probability that a unit will perform a required function under stated conditions for a stated time.

Quantitative Reliability is essential to identify where to focus resources in a system, helping to ensure the riskiest parts of a system gets the attention needed before the failures occur. Even if a system is in production, using a quantitative approach to identifying unreliable components of a system can help prevent costly outages.

A quantitative approach to determining reliability can help with making technical decisions. Which of the multiple approaches will be the most reliable? A quantitate analysis can help the development team make informed decisions based on data, not just past experience or trusting market media.

There are many governance bodies which require risk analysis to be performed on systems. Normally these are for physical systems like medical devices and transportation vehicles, but increasingly software systems are falling under stricter audit requirements. Audit requirements normally include recording data collected during the analysis and therefore imply quantitative approaches. Consider systems which manage the power grid, gas and oil distribution, and financial transactions. There are governing bodies which require software systems have risk analysis performed before and after a system is put into service.

### Reliability Analysis
Every system should undergo some form of risk assessment. This allows the development team to make informed decisions as to the technical direction to take. Being able to ascertain the probability of failure between two or more options will help the team make better decisions and deliver a more reliable product.

There are many who might think this advocates Big, Upfront Design (BUD) which is a common quality of waterfall projects. While BUD often contained risk analysis, it contained far more analysis and often in a very linear, serial fashion. This is not what this article recommends.

Risk analysis can take many forms, and in agile environments, this analysis can be as iterative as any emergent design activity. A risk profile of the design can evolve as the design evolves. It can be a product of the iteration just like user documentation and release notes. In the case of governed systems requiring an audit, the risk analysis may be a formal artifact required before the system can be placed into service.

### How to Predict Reliability
There is a generally accepted approach to predicting the reliability of a system:

1. Enumerate design elements.
1. Determine what can go wrong for each element.
1. Score potential points of failure.
1. Roll-up scores for design elements and processes.
1. Address elements with the highest risk of failure.

This simple, straight-forward approach has been used for many decades to evaluating designs for reliability. It can be performed at any point in a system development life cycle (SDLC) and can be performed iteratively as in sprint planning, or a re-occurring card in Kanban.

This is not a new concept. It is formally known as Failure Mode and Effects Analysis.

## Failure Mode and Effects Analysis
Failure Modes and Effects Analysis (FMEA) is a systematic, proactive method of evaluating a system or process.

FMEA helps to establish the impact of a failure, and identify and prioritize the actions to eliminate or reduce its impact on both the business and its customers. The American Society for Quality (ASQ) defines FMEA as a step-by-step approach to identify all possible failures in a design, manufacturing or assembly process for a product or service.

FMEA was first developed by the US military in the 1940s  to determine the effect of system and equipment failures. In the 1960s it was adopted and refined by NASA and used in the Apollo Space program. During the1970s, Ford Motor Co. introduces FMEA after the Pinto affair and it was soon adopted across the automotive industry.

Today, FMEA is used in manufacturing, aerospace, service and medical industries. There are even whitepapers describing how FMEA can be used to improve patient outcomes by prioritizing courses of treatment.

Recently, FMEA has been used to great success in improving the reliability of complex logic systems and providing management with a tool to more effectively manage resources in improving the reliability of their systems.

### How To Adopt FMEA
The FMEA process is quite simple but can be very detailed. Each development team needs to evaluate to what level FMEA will be applied to their project. This decision will probably be tied to the criticality of the project. FMEA may not need to be too detailed for a plug-in to a blog site. On the other end of the scale, FMEA may need to be very detailed, down to the class and method level, for a system which manages the delivery of medication to a patient or manages the pressure of oil in a pipeline.

#### 1. Identify the components involved in your system
For software systems, this is normally just a UML diagram. Here is an example of an electronic data interchange (EDI) system:

{{< imgproc ComponentModel Fit "2020x668" >}}
Basic component model of an EDI system.
{{< /imgproc >}}

Most will start with the obvious components. These are the assumed design elements; a good place to start.

For some, this is a complete architecture. That is fine, be we are going to perform a reliability analysis and many things affect the integrity and availability of the system.

##### Select Your Use Cases
Use Cases drive discovery of system components. This is true even for existing systems. By walking through a process, it is easier to identify elements in the implementation which may not have been in the original design.

Start with the most obvious use cases and prioritize them. Then for each of the use cases, model the interaction between components. If you are familiar with the unified modeling language (UML) you will probably use Sequence Diagrams as they are one of the most popular ways to model the behavior of system components. Others may use Interaction Diagrams, as they are more like the informal block diagrams depicted in slide decks and the component diagram above.

After walking through multiple use cases, our EDI example yielded a more complete model:

{{< imgproc DeploymentModel Fit "4296x1520" >}}
A more detailed deployment model of an EDI system.
{{< /imgproc >}}

It is often the case that even the development team will not accurately remember all the elements of their design. That is why it is beneficial to walk through a few use cases to "jog" their memory. Sometimes elements were placed in the design without their knowledge. Operations and infrastructure teams will regularly update the deployment environments and may not notify the development teams of the change.

#### 2. Determine Possible Failures For Each Component.
Start anywhere, picking a component and determine all the ways the component can fail or a failure can affect the component. Each of these failures is called a Failure Mode.

Identifying Failure Modes can be predictive or based on past experiences. Look at errors in log files, past trouble tickets and reported defects. The goal is to identify as many, if not all, the potential ways the component can fail.

Things to consider include the component running out of resources (disk, memory, CPU, network bandwidth), suffering a failure of a dependent system (LDAP, DNS, NTP)

##### Assemble a Team
Determining failure modes for a design element is best performed by a team. One person cannot possibly think of every way every component might fail. This team can be the development team, but FMEA works best with a diverse team of developers, operators, users, and stakeholders. This is because each of the failure modes will need to be scored and scoring is biased based on its context. Using a team is a critical success factor for FMEA.

#### 3. Scoring Failure Modes
Traditionally, FMEA involves creating a spreadsheet with each row representing the effects of a failure mode:

| **Item** | **Failure Mode**       | **Effect**                         | **Severity** | **Probability** | **Detection** |
   | -------- | ---------------------- | ---------------------------------- | ------------ | --------------- | ------------- |
   | Firewall | Misconfigured Rules    | IP Spoofing                        | 8            | 2               | 4             |
   | Firewall | Misconfigured Rules    | Entry for External Hackers         | 7            | 2               | 6             |
   | Firewall | Misconfigured Rules    | DDOS Attack                        | 10           | 2               | 2             |
   | Firewall | Encryption Mismatch    | Data will be exposed as plain text | 7            | 2               | 2             |
   | Gateway  | Certificate Expiration | SSL\TLS Handshake Failure          | 4            | 10              | 2             |


Each item in the design or process can have more than one failure mode.  Similarly, each failure mode can have more than one effect. In the above table, we have two components (items), the Firewall and the Gateway. The Firewall has 2 different failure modes: Misconfigured Rules and Encryption Mismatch. The Gateway has one: Certificate expiration.

The Firewall "Misconfigured Rules" failure mode has three effects: IP Spoofing, Entry for External Hackers, and DDOS Attack. Each of the failure effects has been individually scored according to their severity, probability, and detection. They are categorized as follows:

- **Severity** - the seriousness of the effect on the process or design.
- **Probability** - the likelihood of its occurrence. All effects of a failure mode tend to share the same probability score.
- **Detection** - the potential of the failure mode is NOT detected.

Collect the effects of the failure to help determine the severity of the failure. Often there is only one effect and the severity is easy to estimate. As the team discusses the effects of the failure, it may become apparent that the failure is more severe than originally determined. For example; running out of CPU may originally be ranked as a severity of 2 because the effect is the system runs slower, but on further analysis, the process has been observed to freeze completely due to thread starvation and that effect causes the CPU failure to be rated a 7.

Scoring of Failure Mode Effects should follow consistent criteria across the entire project. When comparing design elements, all scores must be relative. This allows the final analysis to determine which elements are the highest risk to the reliability of the system.

It is common for organizations to have standard sets of scoring criteria across all their products and another set for all their processes. The following tables are a starting point for your team.

#### Detectability

| **Detection**        | **Likelihood of DETECTION**                                  | **Ranking** |
| -------------------- | ------------------------------------------------------------ | ----------- |
| Absolute Uncertainty | Control cannot prevent / detect potential cause/mechanism and subsequent failure mode | 10          |
| Very Remote          | Very remote chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 9           |
| Remote               | Remote chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 8           |
| Very Low             | Very low chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 7           |
| Low                  | Low chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 6           |
| Moderate             | Moderate chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 5           |
| Moderately High      | Moderately High chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 4           |
| High                 | High chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 3           |
| Very High            | Very high chance the control will prevent / detect potential cause/mechanism and subsequent failure mode | 2           |
| Almost Certain       | Control will prevent / detect potential cause/mechanism and subsequent failure mode | 1           |


#### Probability
The actual likelihood values can vary from project to project, but the meanings tend to remain consistent across the organization.

| **PROBABILITY of Failure**              | **Likelihood**  | **Ranking** |
| --------------------------------------- | --------------- | ----------- |
| Very High: Failure is almost inevitable | >1 in 2         | 10          |
|                                         | 1 in 3          | 9           |
| High: Repeated failures                 | 1 in 8          | 8           |
|                                         | 1 in 20         | 7           |
| Moderate: Occasional failures           | 1 in 80         | 6           |
|                                         | 1 in 400        | 5           |
|                                         | 1 in 2,000      | 4           |
| Low: Relatively few failures            | 1 in 15,000     | 3           |
|                                         | 1 in 150,000    | 2           |
| Remote: Failure is unlikely             | <1 in 1,500,000 | 1           |

#### Severity
The severity description often differs when analyzing a process or a design. Again, it is important to be consistent across the project.

| **Effect**   | **SEVERITY of Effect**                                       | **Ranking** |
| ------------ | ------------------------------------------------------------ | ----------- |
| Catastrophic | Resource not available / Problem unknown                     | 10          |
| Extreme      | Resource not available / Problem known and cannot be controlled | 9           |
| Very High    | Resource not available / Problem known and can be controlled | 8           |
| High         | Resource Available / Major violation of policies             | 7           |
| Moderate     | Resource Available / Major violations of process             | 6           |
| Low          | Resource Available / Major violations of procedures          | 5           |
| Very Low     | Resource Available / Minor violations of policies            | 4           |
| Minor        | Resource Available / Minor violations of process             | 3           |
| Very Minor   | Resource Available / Minor violations of procedures          | 2           |
| None         | No effect                                                    | 1           |

## Risk Priority Number
The cumulative risk for each design element (item) is ascertained by the Risk Priority Number (RPN). The RPN is calculated by summing the RPN scores for all associated failure modes. The RPN for a failure mode is calculated by taking the highest value from all the associated effects.

In the above example, the Misconfigured Rules failure mode has an RPN score of 120 (S=10 x P=2 x D=6). The Encryption Mismatch RPN is 28 (S=7 x P=2 x D=2). This rolls up to an RPN score of 148 for the Firewall. The Gateway only has one failure mode with one effect and a total RPN score of 80. This means the team needs to pay more attention to the Firewall than the Gateway as the Firewall has a higher calculated risk.

The RPN scores of all the components in a system can then be used to generate a list of elements needing attention prioritized by their risk to the reliability of the system.

Adding up the RPN scores of the all the components of a system or process give the team a system-wide score which can be used to compare that system to other systems, or one design against the other.

## Whoa! This Is Too Much Work!
This is true when FMEA is performed later in the process or after the system is put into service. While it is a common practice to perform FMEA after a system is designed, this is a consequence of waterfall processes.

Besides BUD, there are times when an analysis is performed when an existing process is suffering reliability issues. In these cases, an FMEA team is assembled and a design discovery is performed where each process in the system is analyzed and each design element scored to determine the elements with the highest risk and therefore in need of immediate attention. In these cases, the FMEA team is trying to determine the design elements to address first.

## Iterative Analysis
It is best to keep a model of your system as you go and perform a quick FMEA at each design meeting. For example, each sprint planning meeting has the potential to evolve the design. Before a decision is made, a quick FMEA can be performed to judge if the team is going down the right path. This normally only take 10-15 minutes each meeting and has the added benefit of revealing risk to the entire team. If RPN scores start to rise too fast, the team may need to raise awareness to the product owner or other stakeholders before proceeding. Otherwise, the team may end up delivering a product which is technically correct but unreliable. This would be another case of "built as requested" and not delivering quality product.

Remember, you are only doing enough analysis to enable the next iteration. If you are starting FMEA in the middle of your project, only do enough to enable informed technical decisions for the next iteration. Don't try to catch up unless that becomes a priority for your product owner, and in that case, it will be a product backlog item (PBI).

## Addressing Risk
So what do you do with all these scores? There is nothing wrong with a high RPN score, unless nothing is done to address it. All the work and time invented by FMEA team members will be wasted if nothing is done to address the identified risk.

FMEA generates a list of failure modes. The critical next step is to create compensating controls in the system to address the failure modes. Without these controls, reliability issues will go unchecked.

Using the RPN prioritized list of design elements, the team can begin to create the compensating controls to address the risk in that design element. In the above example, the FMEA team discovered that the certificates will expire on the gateway every year. They may decide to create a compensating control of an automated certificate renewal process to address that risk. This is known as generating an Action, and FMEA with actions is practically worthless.

The agile teams may do this during sprint planning. They discovered a failure mode that can be addressed and generate a PBI and notify the product owner of the new PBI and its importance to the reliability of the system. The product owner can then prioritize the card, possibly for the same sprint. This is how emergent designs can maintain high levels of reliability, by quantifiably assessing the reliability of the system as the design evolves and addressing issues before they become too costly to address later.

## Summary
FMEA is a quantifiable method for assessing the reliability of a process or design. It identifies the most critical elements in a system and allows each risk to be addressed with a compensating control. RPN scores can be used to identify the riskiest elements of a design and to compare alternatives.

FMEA can be very expensive when performed after the fact. Agile methodologies can easily accommodate FMEA as part of normal design iteration. This allows the team to conduct only the necessary analysis to enable the next iteration.

The results of FMEA are wasted if nothing is done to address the identified risk. Actions are generated to create compensating controls for failure modes.