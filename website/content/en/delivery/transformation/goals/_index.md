---
title: Goals
description: >-
    As with all successful projects, setting and monitoring progress toward 
    goals and objectives are critical.
weight: 1
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

## Discovery

Delivery transformation engagements involve a discovery phase to generate goals. This phase requires meeting with not only the delivery teams experiencing issues but also the business stakeholders.

### Meeting with Business Stakeholders

The primary goal of meeting with business stakeholders is clearly understanding their strategic objectives, priorities, and expectations for software development and service management. This meeting helps align technical initiatives with business goals, ensuring that development and service teams deliver value that meets market and customer needs. Stakeholders provide insights into desired outcomes, key performance indicators (KPIs), and regulatory or compliance considerations that may impact system development or operations.

Another critical objective is identifying pain points and bottlenecks in current service delivery from a business perspective. Stakeholders may highlight issues such as delays in feature releases, system downtime affecting customer experience, or inefficiencies in support processes. These discussions help shape improvement initiatives that optimize team performance while aligning with broader business goals.

**Deliverable:** A **Business Goals and Priorities Report** summarizing key objectives, desired outcomes, and identified pain points that need to be addressed by development and service teams.

### Meeting with Delivery Teams

Once we have a picture of the high-level expectations and perceived issues to be addressed, we begin meeting with the delivery teams.

Meeting with the development and service teams is essential to understanding the technical landscape, operational challenges, and constraints they face. The goal is to gain insight into their current workflows, tools, and methodologies, such as Agile, DevOps, or ITSM frameworks. Engaging with these teams makes it possible to identify inefficiencies, process bottlenecks, and areas where automation or tooling improvements can enhance productivity.

Another objective is to bridge the gap between business expectations and technical feasibility. Delivery teams provide a ground-level perspective on what is achievable within given timeframes, budgets, and resource constraints. They can also highlight issues related to technical debt, system reliability, and support workload, which may not be immediately apparent to business stakeholders.

**Deliverable:** A **Delivery Environment Assessment** detailing current development and service workflows, tools, challenges, and opportunities for improvement to enhance efficiency and service quality.

## The Reasons for Change

Who is unhappy?
- Customers
- Team
- Management

Why are they unhappy?

## Delivery Frequency

Many teams are unhappy with how often features are released into production. Some lament having to wait months to release a feature.

The key to mastering more frequent delivery is reducing the scope of a change. The more frequent the delivery cycle, the smaller the change.

Continuous deployment into production involves minimal changes, reducing risk and making spotting issues easier.

### Deliver Implies Production

Delivery implies artifacts are in production. It's not delivered until it is executed in a production environment.

Release management can add latency to production delivery.

Release management may need to be refactored if delivery frequency is an issue.

### Monthly

This is a good goal when just starting out.

Anything longer is just not continuous by contemporary standards.

A.K.A "Little Bang" releases

Monthly releases keep customers happy. However, if you do not have a good deployment process, anything more frequent can annoy customers. If they have to interrupt their workflow to install another release, your product will get in their way.

### Sprintly

This is the sweet spot for most teams.

Mature delivery teams tend to release each sprint. The organization that strives for and can accommodate sprint releases has a more advanced vied or value delivery.

Sprintly releases tend to be the goal for committed teams. When you see a team releasing every sprint, or sooner, you have a team focused on delivery.

When the release process is unobtrusive, this frequency delights users.

The key is to be subtle, releasing only a few features at a time. The product should not change so much that the user has to change their workflow, and training should not be required to use the new feature.

### Weekly

Only one or two features at a time. 

As many bug fixes can fit into a week's worth of work.

### Daily

Typically, only one feature at a time is released daily.

Daily releases are an indication of advanced teams and organizations.

### Hourly

Each release represents one feature, or one addressed defect.

Innovative organizations and expert delivery teams release into production hourly.

## Defect Ratio

For some teams, quality is a concern.

If you are trying to address many defects in your backlog, delivery is not your main issue. Prioritizing quality over everything else is a good place for your team to start. Stop releasing problematic features and adopt a culture of quality first.

## Too Many Cards?

If you have more cards in your backlog than you can hope to release on time, the problem may not be with delivery but with how the backlog is managed.

If cards are taking too long to complete, consider:
- The cards are epics and need to be decomposed.
- The product has technical debt that is getting in the way of delivery.
- The design of the product makes it difficult to maintain

Too many cards in the backlog indicate that the team is focused on delivering work and not delivering value. Scan your backlog and determine the value the customer will receive when completing the card. If it is unclear how the customer directly benefits, then that card may not be focused on value but only represents work. 

A backlog item that represents work and does not provide clear, direct value to the customer should probably be a task or removed from the backlog and placed in a service queue.

The only items in a team's backlog should be features and defects. It is okay if the tool for managing backlog items has concept subtasks associated with features and defects. The team should only count and prioritize feature and defect items representing value delivered to the customer.

What do your customers say? Do they need more features? What are the most important to them? Again, this is not a delivery issue but a backlog management issue. The product owner (or manager) should prioritize the features the customer or market needs and not worry about tracking work or "getting credit for" work.

## Metrics

What metrics is the team trying to affect?

What metrics are essential for delivery teams?

## How to Gather Metrics

A good metric quality is how easy it is to get from the source. Can you call an API in your backlog management tool and get your metrics automatically? Can you set up a scheduled job and collect change management metrics from your change management system?

Generating metrics by hand is not a good idea, as that is time-consuming and error-prone. Metrics could be gathered one way, one time, and another. Data might look "off" and encourage the "fudging" of numbers. Who collects the metrics when team members go on vacation?

Successful teams typically gather metrics by making calls to the API endpoints of their systems of record:
- Backlog Management (e.g., Jira, ServiceNow)
- Source Code Repository (e.g., GitHub, GitLab)
- Artifact Repository (e.g., Artifactory, Nexus)
- Build Orchestration (e.g., Jenkins, Concourse, Argo, GitHub Actions)
- Change Management (e.g., ServiceNow)

Data can be "pulled" by calling the API endpoint of the system of record, but data can be "pushed" to 

### Data Collection Systems

Prometheus is a time series database that is designed to monitor production systems. It is easy to store team metrics in a Prometheus instance.

New Relic is another popular time series database that teams leverage to store metrics about their delivery process. It is a SaaS solution that teams can easily employ to store, retrieve, and analyze metrics of all types.

## How to Display Metrics

It is common for product owners and scrum masters to generate metrics and graphs using tools on their workstations and present the data only during meetings. The problem with that approach is that those who have the most effect on the metrics don't get to see them or see the metrics often enough to change their behavior effectively. 

Team metrics should be "big" and "visible" to everyone on the team. This helps to promote transparency, collaboration, and alignment within the team. Examples of "big visible" practices include using physical boards or digital tools to display project status, progress toward goals, and key metrics. By making information "big" and "visible," team members can quickly understand the project's current state, identify any bottlenecks or issues, and work together to address them effectively.

Implementing "big visible" with remote teams can be challenging. What has worked for many teams with remote members is to have a single landing page for the team. All team meetings start with the facilitator sharing their screen on that page when the meeting begins. That page is a dashboard with links to other important pages like backlogs, documentation sites, notes applications, etc.  When team members log into the network, their landing page is the first thing they see, along with all the essential metrics and links for the team.

Grafana is a free analytics and visualization platform connecting various time series data stores. It allows users to query, visualize, and alert on metrics and logs no matter where they are stored. It supports many data sources, including popular databases, cloud services, and monitoring tools. Grafana provides a user-friendly interface for creating interactive and customizable dashboards that display real-time data in graphs, charts, and tables. It is commonly used in monitoring and observability solutions to help teams gain insights into their systems' performance and health.

New Relic offers a complete analytics and visualization feature set. It is widely used by developers, IT operations teams, and business stakeholders to gain insights into application performance and make data-driven decisions to improve their software applications. Regarding team delivery metrics, New Relic is an excellent solution for making a team's metrics visible to all.

## Determine Baselines

Delivery teams should track metrics over several sprints before making changes to data collection or the process the metric is designed to measure. The team needs to understand its baseline before attempting to make any changes.

## Team Comparisons

It is a common mistake to compare metrics across teams. Every team is unique, and what is the baseline for one team will not be the expected baseline for another.

Managers often make this mistake, thinking the metric applies uniformly to all teams. Experience shows teams have different deliverables, execution environments, processes, restrictions, and dependencies. Every backlog item is different, so trying to "count cards" across teams is meaningless. A medium card for one team is a large card for another. The same is valid for sizing. The team velocity of one team has no relation to the velocity of another team. I know one team that sizes cards far higher than others. A medium card is 25 points for that team.

## Act On Metrics

All team decisions to change the process should be made with the intent to affect a metric positively. That metric is then used to determine whether the decision was good or bad. If the metric starts moving negatively, the team should reverse the decision. If the metric moves positively, the practice should be adopted and part of the team's working agreement or documented practice.

While it is acceptable to adopt an innovative practice, the team should decide how to measure its effectiveness and add it to the data-gathering strategy. A baseline should be established, and the practices monitored for effectiveness.

## Summary

All teams should establish a set of goals and determine how progress is tracked towards that goal. The metrics prove the practice's efficacy, and changes should be made only when the data shows undesirable results.