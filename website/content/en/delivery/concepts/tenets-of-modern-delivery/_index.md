---
title: Tenets of Modern Delivery
description: >-
    Modern delivery builds on decades of agile development, DevOps, DevSecOps, and other contemporary methodologies. 
    Several practices shared by high-functioning teams have been identified, resulting in happy customers and delivery 
    teams.
weight: 1
draft: false
---
These are the beliefs and principles of modern delivery.
1.	There is only one team backlog.
2.	The product backlog tracks customer value; the team backlog tracks work.
3.	Security starts in the backlog.
4.	The team is committed to delivering value continuously.
5.	All processes promote the fastest possible feedback.
6.	Each source code repository represents one deployable artifact.
7.	The simplest branching strategy is preferred; trunk-based development is best.
8.	Every merge to the trunk publishes a release candidate to the artifact repository.
9.	Every build contains tests and static analysis.
10.	Artifacts are semantically versioned.
11.	Snapshots are never deployed.
12.	Build once; deploy many.
13.	Deployments only read from the artifact repository.
14.	Deployments are automated.
15.	Change small, fix small.
16.	Every deployment is tested, even in production.
17.	Roll forward; never roll back.
18.	Refactoring is normal.

# There is only one backlog.
The team has only one source of work, regardless of the number of products supported. This keeps work prioritization simple and keeps the team focused on one delivery stream.

# The product backlog tracks customer value; the team backlog tracks work.
The team exists to deliver value to the customer, not to perform work. Tracking value is different from tracking work.
The product manager is responsible for prioritizing what is valuable to the customer and prioritizing value delivery. The delivery team knows what work is required to release each value increment. Therefore, each product backlog item contains one or more tasks.
The tasks are tracked in the team backlog when the delivery team commits to an iteration.

# Security starts in the backlog.
Security is built-in, not bolted-on. The team ensures that each product backlog item contains a complete understanding of how the changes being introduced affect the system's confidentiality, integrity, and availability. Security is everyone's responsibility.
The entire delivery process contains security considerations. The team considers the system's security from design through implementation, deployment, and finally operation.

# The team is committed to delivering value continuously.
The team understands they exist to deliver value, not to do work. All delivery processes are focused on delivering to production without delay. Any latency in the delivery process is identified and eliminated.

# All processes promote the fastest possible feedback.
Fast feedback acts as a compass, constantly guiding the team towards the right direction, ensuring quality, and enabling them to adapt quickly to change. All workflows, processes, and methodologies enable the fastest possible feedback to the delivery team.

# Each source code repository represents one deployable artifact.
To simplify source code management, source code repositories contain only one deployable artifact. Repositories that contain many modules introduce unnecessary distractions.
Each repository contains one build workflow (continuous integration job) that assembles the source into a deployable artifact, performs static analysis, and unit testing before publishing the verified artifact into the artifact repository. The source repository may contain one or more deployment workflows that retrieve the artifact from the artifact repository, deploy it along with any other required artifacts into an execution environment, and execute system tests to verify the deployment and artifact operation.
Some repositories may not contain source code but contain scripts that assemble artifacts from multiple locations into a new, composite artifact. Examples of these repositories do not contain integration jobs that build artifacts, only the deployment workflows that assemble and configure execution instances. These, strictly speaking, are not source code repositories as they do not contain source code that is compiled into a deployable artifact.

# The simplest branching strategy is preferred; trunk-based development is best.
Branching is only necessary when change isolation is required, and change isolation is only when legacy code review techniques are practiced. Modern delivery practices, such as pair programming and mobbing, reduce the need for branching.
Branching introduces additional work, including code freezes, pulling, resolving merge conflicts, and more. It becomes more difficult to track what value is delivered in which branch.
Simple feature branching is all that modern delivery teams need for a branching strategy.
Trunk-based development removes the need for branching. Eliminating branching encourages pair programming, test-driven development, and small changes.

# Every merge to the trunk publishes a release candidate to the artifact repository.
Every change merged into the trunk generates an artifact that is intended to be released into production. Only testing determines if that artifact makes it that far.
" Snapshot " builds are only used when release management cannot keep up with the pace of delivery and are unnecessary in continuous delivery environments.

# Every build contains tests and static analysis.
Deployment artifacts are only published to the enterprise artifact repository after unit testing and static analysis. All issues identified in analysis and testing terminate the build and prevent publication. False positives are resolved with the same immediacy as defects.

# Artifacts are semantically versioned.
Every change committed to the trunk includes an appropriate increment to the artifact's version. This version is reflected in the artifact's name and carried with it through all deployment activities so it can be easily identified in its execution environment. Semantic versioning is the preferred versioning strategy.

# Snapshots are never deployed.
Delivery teams use snapshot builds to buffer a set of changes before release. Snapshot builds are generally considered under active development and not ready for release. It is difficult to know what features and fixes are contained in a snapshot build and its overall stability. Therefore, no snapshot build is considered stable for release into any execution environment.

# Build once; deploy many.
Each artifact is unique when it is built. Subsequent builds generate potentially different artifacts depending on compiler settings, build environment, and other factors. Any subsequent build is considered a different artifact and should be identified with a different version. Only once a versioned artifact has been validated is it considered ready for deployment.
The DRY principle (do not repeat yourself) emphasizes the importance of reducing repetition, and rebuilding artifacts is considered a waste of time and resources.

# Deployments only read from the artifact repository.
All release candidates of deployable artifacts are published into a secured artifact repository from which deployment processes can reliably retrieve the artifact for deployment.

# Deployments are automated.
Manual deployments are error-prone, time-consuming, inconsistent, and generally inefficient. The delivery team understands the value of delivering their artifacts in an automated manner and the risks involved with delivering their artifacts with human intervention.

# Change small, fix small.
Every merge to the main branch contains the fewest number of changes possible to limit the number of variables between versions. This reduces risk by reducing the complexity of changes to release candidates. This reduced complexity improves testing and debugging activities.
Small changes encourage frequent releases and faster feedback cycles. Frequent deployment of smaller changes allows delivery teams to react to the change's results quicker and provide updates faster. Small changes enable faster delivery.
Modern delivery avoids “big bang” releases where many things change simultaneously. Each release changes only one feature or fixes one defect, delivering value to the user more frequently and with less risk.
Small changes are the least disruptive to the user. Continuous small releases are normally preferred over the potential outages of monolithic releases. Further, smaller changes are less jarring to the user experience, with small changes usually not requiring significant training or modifications to the users' workflow.

# Every deployment is tested, even production.
Once an artifact is published in the artifact repository, it can be deployed into any execution environment. Every deployment undergoes system and integration tests to ensure proper deployment.
Quality Assurance will perform thorough testing in their own execution environments. Artifacts must be deployed to various environments for performance, load, security, and other testing activities. Production deployments are also tested, although these tests are less rigorous and disruptive.

# Roll forward; never roll back.
The team is designed to deliver value frequently and has designed its workflows and processes to address issues within minutes, not days or weeks. When a defect is discovered, the team can deliver a fix immediately.
Because the team has adopted small deployment, static analysis, unit testing, automated deployments, and thorough system testing, the chance of deployment issues is small.

# Refactoring is normal.
The team regularly re-evaluates all aspects of value delivery. The team refactors its design as code changes to gracefully accommodate organic growth. The team adjusts designs as requirements, goals, and objectives evolve to ensure the artifacts fulfill needs and expectations. As culture and organizations change, the team adjusts processes and workflows to help ensure smooth and efficient value delivery.
The codebase is always left in a better state than it was found. This is accomplished by regular refactoring guided by input from peer review and analysis tools.
 
