---
title: Continuous Delivery Maturity Model
description: >-
    There are scores of practices that enable continuous delivery of value to 
    customers. The maturity of a team can be assessed by how many of them have 
    been adopted.
weight: 1
---

{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

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

The Continuous Delivery Maturity Model (CDMM), first published in 2013, provided a structured way to assess and improve an organization’s Continuous Delivery (CD) capabilities. It focused on technical areas such as Build, Deploy, Test & Verification, Information & Configuration, and Governance & Risk, emphasizing automation and reliability in software delivery. Over time, it evolved to include Culture & Organization, recognizing the critical role of leadership, collaboration, and psychological safety in sustaining CD success.

As the industry advanced, the model was further refined into the Continuous Delivery 3.0 Maturity Model (CD3M) [[2](#2)] , which introduces five categories—Continuous Intelligence, Continuous Planning, Continuous Integration, Continuous Testing, and Continuous Deployment—and five maturity levels: Foundation, Novice, Intermediate, Advanced, and Expert. CD3M emphasizes data-driven decision-making, observability, and AI-driven automation, aligning with modern DevOps and cloud-native approaches.

This evolution from CDMM to CD3M reflects the shift from focusing solely on technical automation to a more holistic, strategic, and intelligent approach to software delivery. CD3M provides organizations with a roadmap for achieving scalable, resilient, and efficient CD pipelines, integrating modern trends such as continuous monitoring, cloud architectures, and end-to-end automation.

The model described here has taken a parallel evolutionary path, drawing from both models and tested through application with many teams of different types. Additionally, this model includes all types of delivery teams, not just software development teams.

## Maturity Levels

The  Continuous Delivery Maturity Model [[1](#1)] contains five levels of maturity:
- **Base:** This is the starting point for a team’s journey towards continuous delivery. At this level, little or no automation is in place, and updates are delivered infrequently and with significant manual effort.
- **Beginner:** The team has implemented basic automation of its delivery processes, such as automated builds and testing. However, these processes are not yet integrated into the overall delivery workflow.
- **Intermediate:** The team has integrated automation into its delivery workflow and begun implementing continuous integration and continuous testing. However, deployment to production is still done manually and infrequently.
- **Advanced**: The team has implemented continuous deployment and begun experimenting with different deployment strategies. Additionally, it will monitor and measure the performance of the systems in production.
- **Expert:** The team has fully embraced continuous delivery and established a culture of continuous improvement. It will continuously monitor and optimize its delivery process and regularly release new features and updates to its customers.

## Categories
The original model contained five categories of practices. It has evolved to include six categories. Each category includes numerous identified good practices for delivering value to customers.

### Culture and Organization

This is the environment of continuous delivery. It focuses on collaboration, leadership support, psychological safety, continuous learning, and team alignment. A strong culture enables teams to take ownership of the software delivery process and continuously improve.

### Design and Architecture

Practices in this category relate to structuring your products for success, quality, and user satisfaction. This category deals with the flexibility and scalability of software architectures and infrastructure. As maturity increases, organizations move toward modular, cloud-native architectures, infrastructure as code (IaC), and automated environment provisioning.

### Build and Deploy

This category of practices encompasses everything related to building your artifacts and delivering their value to the user. It also covers the automation of software builds and deployments. Maturity in this category means moving from manual, error-prone processes to fully automated, repeatable, and reliable build and deployment pipelines.

### Testing and Verification

Practices in this category relate to ensuring the quality of artifacts. They also encompass automated testing practices, ensuring that software changes are validated quickly and reliably. High-maturity organizations have extensive automated test suites covering unit, integration, system, and performance testing.

### Information and Reporting

Practices related to measuring the success, progress and performance of your artifacts are included in this category. Covers observability, proactive monitoring, and incident response. High-performing organizations have real-time visibility into system performance, automated alerting, and data-driven decision-making to improve reliability and resilience.

### Security and Risk

Focuses on compliance, security, and risk management. Maturity in this area involves integrating security and compliance checks into the continuous delivery pipeline, ensuring fast and safe releases while meeting regulatory requirements.


## References
<ol>
  <li id="1">Andreas Rehn and Patrik Boström,The Continuous Delivery Maturity Model,Feb 2013, online: <a href="https://www.infoq.com/articles/Continuous-Delivery-Maturity-Model/">InfoQ</a></li>
  <li id="2">Netherlands National Institute for the Software Industry (NISI), Continuous Delivery 3.0 Maturity Model (CD3M), online: <a href="https://nisi.nl/continuousdelivery/articles/maturity-model">NISI</a></li>
</ol>