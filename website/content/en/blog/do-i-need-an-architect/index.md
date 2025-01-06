---
date: 2018-12-17
title: Does My Project Need A Software Architect?
linkTitle: Do We Need an Architect?
description: >
  Project managers often contact the enterprise architecture team and ask, "Do 
  I need an architect for my project?" The answer is simple. Every project has 
  an architect, whether or not they are titled as such. The real question is how 
  much time should your project dedicate to architectural decisions.
author: Steve Cote ([@sdcote.com](https://bsky.app/profile/sdcote.com))
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---

All systems have an architecture, and every team makes architectural decisions. Many technical decisions made by a team affect the "architecture" of the system whether they realize it or not. So all development teams will be architecting their systems.

The challenge for the organization will be if these teams have all the information to make the correct decisions. Technical leads are often experienced enough to make the correct technical decisions for the team and can help guide the development, but Tech Leads are usually too busy with team backlogs to properly coordinate with other stakeholders, departments, teams and to do the research to make the best technical decisions for the organization as a whole. Tech Leads normally have a limited scope of influence and do not have the time to coordinate technical decisions with other parts of the organization.

## Architectural Decisions
An architect is a role, although many mistake it as a level of expertise. The role of the architect is to identify the important characteristics (a.k.a. qualities) of the system and guide technical decisions to keep the system in line with those characteristics. Small development teams can successfully make all the architectural decisions themselves, just like large teams. The challenge teams have is to find the time to identify the important qualities of the system and all the factors affecting them.

Few systems run completely independent from the rest of the organization and most are affected by external factors.  There are many things which will affect the cost of the system to develop, operate and maintain. It is easy for the cost of the system to exceed the value it provides and this is another time when projects fail. So it is possible for a team to make all the correct technical decisions to deploy the project, but find out later that the system is too costly to operate and maintain or that operational costs now make the project unprofitable. This is because the long-term operational qualities of the system were not taken into account when technical decisions were made.

Understanding the important qualities of the system and managing all the factors affecting those qualities takes time and effort. As the size and complexity of a project increases, so to does the effort involved in making informed decisions and the cost of making a mistake. This is why the role of an architect is assigned to someone who is dedicated to the tasks involved.

## Agile Versus Waterfall
This is not an "agile" versus "waterfall" issue. It is making the right technical decision by gathering all the information and making a deliberate trade-off analysis and not making a technical decision based solely on how quickly the feature can be delivered.

Architecture decisions are regularly made regardless of the methodology being used. Agile teams make architecture decisions just as teams who practice traditional waterfall development. Remember, all systems have an architecture, even those written by one person. It's just that one person made all the architectural decisions.

Agile teams are often pressured to deliver value quickly. They are incented to make architectural decisions whcih favor quick delivery over low total cost of ownership. There are also teams who deliberately make technical decisions to keep them busy, keep the project alive. The main system qualities the design decisions are enabling is usually only reduced time to market. Few other system qualities are considered on agile teams.

The concept of DevOps has helped to keep the development team focused on the long-term cost of operating the system as it will be the development team who will be paged when the system has a defect. Because poor architectural decisions will ultimately affect the DevOps team, the architecture decisions will normally take into account the ease of operation and maintenance along with time to market. This is a step in the right direction, as technical decisions are taking more system qualities into account.

The development methodology has little to do with the need for an architect. It is what qualities the team take into account when making their design decisions.

## Cost of Getting It Wrong
Making the wrong technical decisions can be costly in many ways. The project can experience delays as selecting the wrong technology can make updates and modifications more difficult. As the load on the system grows, it may become more costly to sustain growth or to reliably support increased transaction rates. If something fails, the architecture can prevent quickly spotting and resolving defects. The architecture can make operations far more expensive in time and computing resources than planned. The wrong architecture can expose data to attack, corruption, unauthorized access compromising the overall security of the system. One security breach, one outage can be very expensive for a company both in reputation and financially.

Fixing an issue while a system is in development is far less expensive than when it is in production. What might be a minor defect when there are dozens of users on the system becomes a major defect when the system is supporting thousands of users and has other systems relying on it. Identifying and addressing issues on the drawing board is far less invasive than repairing a system which is supporting actively supporting the revenue of the company.

Design decisions also affect how much the system costs to run, maintain and update over its life. There are many systems which were relatively easy to develop, but now costs far more than normal to keep running. Design decisions made to get the project out the door on time are now costing the company far more to operate and maintain than their deliberately architected counterparts. The time spent in remediation far outweighs the time spent in performing a deliberate trade-off analysis.

Just remember, the cost of making the wrong decisions on small projects is usually also small. Likewise, making the wrong architectural decision on larger projects is more expensive. So the answer to the architect question is one of risk management.

Do you want to risk making important technical decisions without taking the time and effort to coordinate with other teams, customers, vendors, industry, and the organization as a whole? Or would it be safer to dedicate a resource to helping avert technical costs over the life of the system?

## The Result
Most project managers allocate some budget for architecture duties to be performed in their projects. This can be in the form of a resource from another team (e.g. enterprise architecture) of an additional team member to account for the architectural activities the entire team will perform in the delivery of the system. This gives the team time to dedicate to performing architectural tasks and not just make design decisions on getting features "out the door."

Does your project need an architect? It already has at least one. The real question is if the team is given the time, information and incentives to make the correct architectural decisions for the projects entire life.