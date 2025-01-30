---
title: Good vs Best Practices
description: >-
  Many use "Best Practice" to describe the preferred way to do something, but most
  problem domains do not have best practices. There are "Good Practices" that should
  be used instead. But what is the difference between "Good" and "Best" practices?
weight: 1
---

The term best practice is misused more often than not. It is a "hand-wavy" phrase that is meant to cover everything from documented practices to "trust me" I know what I'm talking about." Its misuse has led some to dismiss the term as so much double talk, and rightly so. Continue misusing a term long enough, and it will lose its meaning and value.

In the late 1990s, Dave Snowden, an IBM Fellow in knowledge management, created a knowledge model called Cynefin [[1](#1)]. It was initially developed to help organizations better understand and manage knowledge. Over time, it evolved into a broader decision-making and sense-making framework [[2](#2)] that helps leaders navigate complexity and uncertainty. This framework evolved over the years and became widely adopted in agile development, public policy, and crisis management fields.

## Problem Domains
A problem domain is a subject area or context in which a problem is identified, analyzed, and solved. This includes everything from "my coffee maker won't brew a cup of coffee" to landing humans on Mars. Are you trying to deliver quality software to your customers? Then, your problem domain is software delivery. Do you have too many defects in your code? Then, software quality is your problem domain. Delivering a new product or service to a market is also a problem domain.

Problem domains are containers for other problem domains. Decomposing problems into subdomains is essential to effectively addressing problems and collaborating on their resolution. Troubleshooting a circuit may not contain many problem domains, but landing a spacecraft certainly does. One person can effectively troubleshoot a circuit, but it will take one person a lifetime to address every problem domain in landing a spacecraft.

Managing a problem involves determining its domain and applying a management strategy for that domain. It does not matter what the problem is; all problems start in a state of confusion and cycle through at least four states until they become consistently manageable with best practices. What state a problem domain is in depends on our understanding of the cause-and-effect relationships within that domain.

## Cause an Effect
When we enter a problem domain, we seek cause and effect. What practices (causes) result in the desired outcomes (effects)? When we talk about practices, we are talking about what we will _do_ to achieve the desired outcome.

The understood relationships between causes (practices) and effects (outcomes) determine the type of problem domain we are in and how we operate in that domain. Therefore, we must be aware of what type of problem domain we are in so we can respond accordingly, as each type of problem domain takes a different approach to achieving desirable outcomes.

### Confusion

Everything starts within a state of disorder or "Confusion"; decision-makers are unaware of which domain they’re currently in or what practices should be applied. This is a transitional state, with the goal of moving into a known state or domain.

Some call this state "Apathy," when organizations or individuals fail to engage with complexity. This happens when decision-makers ignore or avoid classifying problems, leading to inaction or mismanagement. If leaders do not work to clarify and categorize a situation, they may fall into decision paralysis, complacency, or disengagement, which aligns with the concept of apathy.

### Chaos
When we first enter a problem domain, we tend not to see any patterns. Even in well-known problem domains, the participants and circumstances may have changed sufficiently to make the domain unrecognizable, at least initially.

When in a chaotic problem domain, we prioritize acting to change our situation—failure to act results in failure to change. Our goal is to move into a more predictable situation or simply to get out of danger.

If we take some action, we may not see what effect it has. This is most often due to not knowing what to observe. In a chaotic problem domain, cause and effect are unclear. We do not yet know what to monitor to sense our situation.

When in the chaotic problem domain, we try something and see how it affects our domain. These **Novel Practices** are new and untested, but once tried, we sense their effect on our domain and respond with additional new practices until we begin to see patterns. We begin categorizing these Novel Practices into those that result in desirable outcomes and those that result in undesirable consequences. In this stage, we **act**, **sense** the results, and **respond** accordingly.

Once we begin to see patterns and indications of cause and effect, we enter a new problem domain: complex.

### Complex
In complex problem domains, we take Novel Practices with positive outcomes and evolve them into more effective **Emergent Practices**. We still do not know what we don't know, but we perform experiments based on our observations. We probe the domain, sense its state, and respond accordingly.

Since this is the domain of experimentation, methodologies like SCRUM work in this domain. Teams discover an issue and respond by modifying their current practices.

In complex problem domains, our actions change the situation in unpredictable ways. The relationships between cause and effect are still unknown but are becoming more apparent. Once those relationships become reproducible, we enter the following type of problem domain: complicated.

### Complicated
In "Complicated" problem domains, the relationship between cause and effect requires analysis or expertise, and we rely on experience to guide us toward desirable outcomes. This is because a range of correct answers brings varying degrees of success.

This is where **Good Practices** are used because we know from experience that some practices will result in positive outcomes. Agile methodologies such as Kanban, Disciplined Agile Delivery (DAD), and Lean work well in this domain because the tasks are known in these methodologies; we have estimates for their duration and a general order of when things should be done.

Software development is an example of a complicated problem domain. There are many right ways to do things, and experience is required to know what practices will most efficiently achieve the desired outcomes in the current environment.

### Clear
In "Clear" or simple problem domains, the relationship between cause and effect is clear: if you do X, you will get Y. This means there are rules to achieve desirable outcomes. 

This is the domain of **Best Practices**, standard operating procedures, and practices that have been proven to work to achieve consistent results. In this problem domain, one finds the proper rule and applies it.

In this domain, waterfall methodologies are acceptable as everything about the problem, such as what tasks need to be completed and how long they will take, is known. This fits well with the methodology built around a particular scope, estimates, and task order.

The challenge we often face is that not all problem domains have clear and consistent cause-and-effect relationships. There are too many variables in most problem domains to manage effectively, and it is difficult to identify best practices for all problem domains.

## Applying Practices
Initially, we are in a state of confusion. We do not know what type of problem domain we are in. The goal is to move into a domain where we can apply practices to achieve the desired outcomes. This is easiest in the Clear or simple domain where we can consistently apply Best Practices to achieve desired outcomes. Still, not all problem domains have consistent cause-and-effect relationships. Sometimes, the best we can do is move our problem domain to a Complicated domain and rely on experts to guide us to desirable outcomes.

As we manage our situation from confusion to chaos, we begin experimenting with **Novel Practices**. We act first, then sense the response to our actions to determine our subsequent response. After enough iterations of "act-sense-respond," we begin to spot cause-effect relationships and gradually move into the complex problem domain.

As we move from "chaos" to "complex" domains, we probe our environment to sense our situation and respond with **Emerging Practices** that evolve with our understanding of the problem domain. We continue this "probe-sense-response" cycle until we identify more consistent cause-effect relationships and gradually move into the Complicated domain.

Moving our problem domain from "Complex" to "Complicated," we sense our situation, analyze what **Good Practices** we can apply, and respond with a known practice to achieve an expected result. Through experience and expertise, we continually apply known practices to achieve an expected result. We cycle through multiple iterations of "sense-analyze-respond" until we find a consistent mapping of practices that achieve consistent, desirable outcomes and move our problem domain into the "Clear" domain.

As we move our problem domain from "Complicated" to "Clear," we identify **Best Practices** that can be used to achieve desired outcomes. In Clear or simple problem domains, a known practice is mapped to a known outcome. It then becomes a matter of sensing the situation, categorizing it, and responding with a known best practice—the cycle of "sense-categorize-respond" results in consistent, desirable outcomes.

## Complacency
Once a problem domain is successfully moved into the "Clear" domain, it is easy to become complacent. Problem domains do not remain constant. It is easy for a problem domain to move quickly from "Clear" to "Chaotic," particularly in technical and business domains. 

Management must continually reassess their problem domain and look for inconsistencies indicating that practices (causes) require updating to account for changing environmental factors. Failure to respond quickly to changing problem domains will result in undesirable outcomes, moving the domain into chaos.

When introducing a new factor, a "Clear" problem domain may shift into a "Complicated" domain. Consider a manufacturer that must deal with a new competitor. The practices that worked for the manufacturer in the market may not work with new competition. Management must determine what new practices must be created to achieve the desired outcomes. Good practices like improving customer service may address the issue. 

A changing problem domain sometimes requires Novel/New practices to move it toward more consistent outcomes. A product may require redesign to meet market expectations, and customer service may need to offer new services to maintain customer satisfaction. A new competitor or technology can quickly turn a long-time "Clear" domain into "Chaos" overnight, and management needs strategies to respond.

It should be noted that all domains can change. When you think you have a set of **Good Practices** for a **Complicated** domain, an external factor can send your problem domain into chaos. What used to be considered good practices in data processing no longer apply in today's technology environment. Virtual Machines used to be considered good practices, but with the wide acceptance of containerization, VMs are no longer considered a good practice.

## Review
Finding and applying the appropriate practice depends on the type of problem domain you are in.

All problem domains start in a transitional state of "Confusion" (Apathy) – When it's unclear which domain applies, requiring further assessment to classify the situation correctly and progresses through at most four basic states:

- **Chaotic**
  - Unknown or decoupled cause-effect relationships - act or fail.
  - Strategy: act-sense-respond
  - **Novel** Practices
  - Example: Responding to a natural disaster or a cybersecurity breach.
- **Complex**
  - Loosely coupled cause-effect relationships - involve experimentation.
  - Strategy: probe-sense-respond
  - **Emergent** Practices
  - Example: Managing a company culture shift or handling a pandemic response.
- **Complicated**
  - Known cause-effect relationships - requires expertise.
  - Strategy: sense-analyze-respond
  - **Good** Practices
  - Example: Fixing a car engine, where an expert can diagnose and solve the issue.
- **Clear**
  - Tightly-coupled cause-effect relationships - clear approach to desired outcomes.
  - Strategy: sense-categorize-respond
  - **Best** Practices
  - Example: Following a standardized process, like assembling furniture with clear instructions.

Complacency - No problem domain is static. Change is inevitable, and it can occur gradually or overnight. Management must continually assess their problem domain and apply the appropriate strategy to achieve desired outcomes.

## References
<ol>
  <li id="1">Snowden, David (1999). "Liberating Knowledge", in *Liberating Knowledge*. CBI Business Guide. London: Caspian Publishing.</li>
  <li id="2">Snowden, David J.; Boone, Mary E. (2007). <a href="https://hbr.org/2007/11/a-leaders-framework-for-decision-making">"A Leader's Framework for Decision Making"</a>*Harvard Business Review*. **85** (11): 68–76.</li>
</ol>