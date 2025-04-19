---
title: Continuous Delivery Maturity Model
description: >-
    There are scores of practices that enable continuous delivery of value to 
    customers. The maturity of a team can be assessed by how many of them have 
    been adopted.
weight: 2
---

Years of coaching teams have revealed a set of good practices for delivery teams. These practices have proven to improve quality and reduce time to market.

Successful teams have adopted these practices where appropriate, and mature teams have adopted more. Modern delivery practices use a Continuous Delivery Maturity Model to assess a team's baseline and, with the team's participation, begin adopting good practices from the model.

After each iteration, the team assesses its progress against the model and adopts additional practices that may help achieve the team's goals.

## Origins

 [Andreas Rehn](https://www.infoq.com/profile/Andreas-Rehn/), [Patrik Boström](https://www.infoq.com/profile/Patrik-Boström/), and [Tobias Palmborg](https://www.infoq.com/profile/Tobias-Palmborg/) conceived the Continuous Delivery Maturity Model [[1](#1)] and published it in 2013.

One of my larger clients had adopted the model and created a "rainbow chart" distributed to all its development teams. As we coached teams in modern delivery practices, we used that chart to gauge their progress. As more teams were engaged, the "rainbow chart" was expanded to a list of good practices delivery teams used to improve their value delivery.

All the delivery coaches participated in evolving the list. After several months of coaching teams, over 100 good practices were identified. Data Science teams, traditional "code and compile" teams and service teams benefited from examining and adopting these practices. Since we coached many different team types, good practices from all types were added to the model.

As part of each team's coaching engagement, coaches would sit with the team for an iteration (sprint) and set baselines for several delivery metrics, document a team's workflow, and assess the team's "delivery maturity." We then assisted the teams with implementing promising delivery practices from the list. We reported back to stakeholders on the teams' progress in delivery at the sprint review and customer demonstrations.

The client's "rainbow chart," based on the Continuous Delivery Maturity Model [[1](#1)], has evolved into a valuable coaching tool that draws on the experiences of numerous coaches and various types of teams, proven through the application of many team engagements. 

### Evolution

The Continuous Delivery Maturity Model (CDMM), first published in 2013, provided a structured way to assess and improve an organization’s Continuous Delivery (CD) capabilities. It focused on technical areas such as Build, Deploy, Test and verification, Information and configuration, and Governance and risk, emphasizing automation and reliability in software delivery. Over time, it evolved to include Culture and organization, recognizing the critical role of leadership, collaboration, and psychological safety in sustaining CD success.

As the industry advanced, the model was further refined into the Continuous Delivery 3.0 Maturity Model (CD3M) [[2](#2)], which introduces five categories—continuous Intelligence, Continuous Planning, Continuous Integration, Continuous Testing, and Continuous Deployment—and five maturity levels: Foundation, Novice, Intermediate, Advanced, and Expert. CD3M emphasizes data-driven decision-making, observability, and AI-driven automation, aligning with modern DevOps and cloud-native approaches.

This evolution from CDMM to CD3M reflects the shift from focusing solely on technical automation to a more holistic, strategic, and intelligent approach to software delivery. CD3M provides organizations with a roadmap for achieving scalable, resilient, and efficient CD pipelines, integrating modern trends such as continuous monitoring, cloud architectures, and end-to-end automation.

The model described here has taken a parallel evolutionary path, drawing from both models and tested through application with many teams of different types. Additionally, this model includes all kinds of delivery teams, not just software development teams.

## Maturity Levels

The  Continuous Delivery Maturity Model [[1](#1)] contains five levels of maturity:
- **Base:** This is the starting point for a team’s journey towards continuous delivery. At this level, little or no automation exists, and updates are delivered infrequently and with significant manual effort.
- **Beginner:** The team has implemented basic automation of its delivery processes, such as automated builds and testing. However, these processes are not yet integrated into the overall delivery workflow.
- **Intermediate:** The team has integrated automation into its delivery workflow and begun implementing continuous integration and continuous testing. However, deployment to production is still done manually and infrequently.
- **Advanced**: The team has implemented continuous deployment and begun experimenting with different deployment strategies. Additionally, it will monitor and measure the performance of the systems in production.
- **Expert:** The team has fully embraced continuous delivery and established a culture of continuous improvement. It will continuously monitor and optimize its delivery process and regularly release new features and updates to its customers.

## Categories
The original model contained five categories of practices. It has evolved to include six categories. Each category includes numerous identified good practices for delivering value to customers.

### Culture and Organization

This is the environment of continuous delivery. It focuses on collaboration, leadership support, psychological safety, continuous learning, and team alignment. A strong culture enables teams to take ownership of the software delivery process and continuously improve. Organization and culture are critical to creating an effective and permanent continuous delivery environment.

The base level is generally characterized as a culture that has adopted some agile methodologies but still struggles with traditional processes and governance. Beginning-level teams have started adopting a culture of breaking traditional barriers. Intermediate-level teams are comfortable being open and collaborative and continually use metrics to improve their processes. Advanced teams deliver and maintain their artifacts in all environments, including production. Expert teams promote their advanced practices across the organization, simultaneously sharing and learning with other teams.

### Design and Architecture

Practices in this category relate to structuring your products for success, quality, and user satisfaction. This category deals with the flexibility and scalability of software architectures and infrastructure. As maturity increases, organizations move toward modular, cloud-native architectures, infrastructure as code (IaC), and automated environment provisioning.

The design and architecture of products and services will have an essential impact on the ability to adopt continuous delivery. The journey will be much smoother if a system is built with continuous delivery principles and a rapid-release mindset from the beginning.

The design and architecture of software products are essential for implementing Continuous Delivery. If a product has been designed with fast and high-frequency delivery principles, the step to Continuous Delivery is much easier. For many companies, completely redesigning existing systems is not an attractive option. That is why Design and Architecture are included as separate categories in the Maturity model.

### Build and Deploy

This category of practices encompasses everything related to building your artifacts and delivering their value to the user. It also covers the automation of software builds and deployments. Maturity in this category means moving from manual, error-prone processes to fully automated, repeatable, and reliable build and deployment pipelines.

A controlled build process regulates the steps that retrieve, build, package and store the source code.

Deploying is moving software to where it can be tested, accessed by a user, or ready to be sent to a customer.

Build and deployment are core to Continuous Delivery and Deployment. This domain is where tools and automation first come into the process.

Build and deployment are the core of continuous delivery, where many tools and automation find applications in the deployment pipeline. This is often the point that is first considered when it comes to Continuous Delivery. At first sight, an adult delivery pipeline can seem very overwhelming. The complexity of the pipeline is highly dependent on the degree of maturity of the organization's current build and deployment process. This category describes a logical growth model with which structure and understanding of the different levels are considered.

### Testing and Verification

Practices in this category relate to ensuring the quality of artifacts. They also encompass automated testing practices, ensuring that software changes are validated quickly and reliably. High-maturity organizations have extensive automated test suites covering unit, integration, system, and performance testing.

Continuous Integration and Delivery have long been associated with some level of automated testing. This is true in the seminal article by Martin Fowler  [[3](#3)] and in the older practice described by Steve McConnell of the Daily Build and Smoke Test  [[4](#4)]. The developer must receive rapid feedback on quality problems, so regular builds and deployments are conducted to receive that feedback frequently throughout the development cycle.

Testing is critical for successful software development and is a core component of the successful implementation of Continuous Delivery and Deployment. Like Build & Deploy, maturity in this category will involve tools and automation.

This category is potentially the most critical area the team should focus on. Testing and Verification relate directly to the quality of the service delivered to the team’s user community and influence how much rework the team performs in the areas of defects and incidents.

Manual testing is time-consuming, inefficient, and error-prone. The drudgery of manually testing the system causes the team to perform testing less often than it should. The result is that regression testing is performed infrequently, which delays timely updates to the system software. The team has several versions behind the vendor’s current release, which is depriving users of valuable features and potentially serious security fixes. The team’s priority should be to execute testing promptly and efficiently to promote more frequent testing.

Similar to the Build and Deploy category of practices, maturity in this category will involve tools and automation. However, it is also important to constantly increase the system's test coverage to build confidence in speed with frequent releases. Usually, tests involve verifying expected functionality according to requirements differently, but verifying the expected business value of released features is equally important.

### Information and Reporting

This category includes practices related to measuring your artifacts' success, progress, and performance. It covers observability, proactive monitoring, and incident response. High-performing organizations have real-time visibility into system performance, automated alerting, and data-driven decision-making to improve reliability and resilience.

Reporting covers information about the quality and content of an organization’s software and metrics relating to the Continuous Delivery process.

It is also essential to have access to information needed to measure and continuously improve the process.

Any business process includes a specific information set that can be reported on; the process of developing and releasing software is no exception, and the set of information that is handled in this particular area would typically include concepts like component, requirement, version, developer, release, environment, etc. In this category, we want to show the importance of handling this information correctly when adopting Continuous Delivery. The information must, e.g., be concise, relevant, and accessible at the right time to the right persons to obtain the full speed and flexibility possible with Continuous Delivery. Apart from information directly used to fulfill business requirements by developing and releasing features, it is also essential to access information needed to measure and continuously improve the process.

The team needs a framework for collecting and storing metrics of all types for easy correlation and analysis. This framework should collect, store, and generate alerts when metrics are observed outside the team's established thresholds. 

A wide variety of applications can perform these functions, some licensed, many free. It is suggested that the team look into free monitoring frameworks such as [Prometheus](https://prometheus.io/), which can be implemented in a few hours and provide excellent application performance monitoring at minimal cost.

Prometheus can be easily paired with a free dashboard tool like [Grafana](https://grafana.com/), which allows the team to perform various analytics and visualizations on collected data. Grafana dashboards can be created to show performance metrics and any metrics the team gathers, including those generated from testing frameworks and other CI/CD tools. The entire delivery process can be instrumented to push metrics to the team's dashboards for regular monitoring.

### Security and Risk

Focuses on compliance, security, and risk management. Maturity in this area involves integrating security and compliance checks into the continuous delivery pipeline, ensuring fast and safe releases while meeting regulatory requirements.

This set of practices relates to the team’s emphasis on identifying and mitigating risk throughout the development process. This contrasts with addressing risk only after the product artifacts are built and employed in a production environment.

By addressing risk early and often throughout the entire delivery process, the teams ensure security is built into the final product. This reduces the costs related to mitigating risk later when the mitigation costs are usually much higher. Security “built-in,” instead of “bolted-on,” ensures release schedules are met, and costs remain steady for the system's development, deployment, operation, and ongoing maintenance.

This category does not often come to mind when thinking about continuous delivery, but security and risk are related directly to the quality of the product or service. It is much easier to provide insecure products and services than to ensure updates to the system do not compromise the organization's security. Supply chain attacks are widespread and have affected thousands of organizations, causing significant financial loss and risking physical safety. It is, therefore, critical that all delivery practices, continuous or otherwise, focus on the integrity of their processes.

The security of a system is everyone’s responsibility. From the system user to the product owner and business analyst who defines the acceptance criteria of the cards, to the developers who alter the system, and to the testers who validate the effectiveness of the changes. To the system operators who ensure only validated product artifacts are deployed to the execution environment, all are responsible for the security of the solutions deployed to all environments, not just production. Security is not somebody else’s job. 

Security should be built into every application and solution, not bolted on later. Every feature should include security acceptance criteria. Every request must be evaluated to ensure its fulfillment does not adversely affect the organization's security posture. There should be at least one misuse case for every use case. Every card should have acceptance criteria and failure criteria.

Security testing should be part of every team's testing plan. Teams can employ various penetration testing tools, many of which are free and open-source, to validate their security posture. With continuous delivery, security testing should be performed as an ordinary part of the automated delivery pipeline. Nightly destructive penetration tests can be performed using automated tools and virtual compute instances like the cloud and Docker containers. Teams should take the time to include security in all their CI/CD pipelines.

The security of a system is composed of three main system qualities:

*  **Confidentiality** – the ability of the system to prevent unauthorized access.
* **Integrity** – the ability of a system to operate as designed.
* **Availability** – the ability of the system to remain ready and able to perform its function.

The security of the system is not only about unauthorized access. Anything that affects the above qualities is considered a security issue. This includes performance degradation affecting the system's ability to provide its function in the required time or anything that causes the user to affect the availability, such as entering multiple long queries that slow the system to prevent timely responses from other users.

This category of practices is the weakest for most teams due to a lack of security training and a culture that lets corporate cybersecurity handle all security initiatives.

## Summary

The Continuous Delivery Maturity Model (CDMM) is a framework that helps organizations assess and improve their software delivery capabilities by focusing on key areas such as automation, testing, deployment, governance, culture, and monitoring. As it has evolved into the Continuous Delivery 3.0 Maturity Model (CD3M), it now integrates data-driven decision-making, intelligent automation, and strategic planning, aligning with modern DevOps and cloud-native practices. By advancing through its maturity levels, organizations can deliver value faster, more frequently, and with higher quality, reducing risks, improving collaboration, and ensuring that software is reliable, scalable, and continuously improving.


## References
<ol>
  <li id="1">Andreas Rehn and Patrik Boström,The Continuous Delivery Maturity Model,Feb 2013, online: <a href="https://www.infoq.com/articles/Continuous-Delivery-Maturity-Model/">InfoQ</a></li>
  <li id="2">Netherlands National Institute for the Software Industry (NISI), Continuous Delivery 3.0 Maturity Model (CD3M), online: <a href="https://nisi.nl/continuousdelivery/articles/maturity-model">NISI</a></li>
  <li id="3">M. Fowler, "Continuous Integration," 01 May 2006. [ <a href="https://martinfowler.com/articles/continuousIntegration.html">Online</a>].</li>
  <li id="4">S. McConnell, "Daily Build and Smoke Test," July 1996. [<a href="https://stevemcconnell.com/articles/daily-build-and-smoke-test/">Online</a>]. </li>
</ol>