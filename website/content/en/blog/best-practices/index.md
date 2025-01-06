---
date: 2018-10-06
title: Good versus Best Practices
linkTitle: Good versus Best Practices
description: >
  Many use the term Best Practice to describe the preferred way to do something but 
  many problems domains do not have best practices. There are Good Practices that 
  should be used instead. But what is the difference between Good and Best practices?
author: Steve Cote ([@sdcote.com](https://bsky.app/profile/sdcote.com))
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---
## Problem Domains
The term best practice is misused more often than not. It is a "hand-wavy" phrase that is meant to cover everything from documented practices to "trust me I know what I'm talking about." Its misuse has led some to dismiss the term as so much double talk and rightly so. Continue misusing a term long enough and it loses its meaning and value.

A problem domain is a subject area or context in which a problem is identified, analyzed, and solved. This includes everything from "my coffee maker won't brew a cup of coffee", to landing humans on Mars. Are you trying to deliver quality software to your customers? Then your problem domain is software delivery. Do you have too many defects in your code? Then, software quality is your problem domain. Delivering a new product or service to a market is a problem domain.

Problem domains are containers for other problem domains. Decomposing problems into subdomains is an important step to effectively addressing problems and collaborating on their resolution. Troubleshooting a circuit may not contain many problem domains, but landing a spacecraft certainly does. One person can effectively troubleshoot a circuit, but it will take one person a lifetime to address every problem domain in landing a spacecraft.

Managing a problem is determining what in what domain it is and applying a management strategy for that domain. It makes no difference what the problem is, all problems start in a state of confusion and cycle through at least 4 states until it becomes consistently manageable with best practices. What state a problem domain is in depends on our understanding of the cause-and-effect relationships within that problem domain.

## Cause an Effect
When we enter a problem domain, we are looking for cause and effect. What practices (causes) result in the desired outcomes (effects). When we are talking about _practices_ we are really talking about what are we going to _do_ to achieve the desired outcome.

The understood relationships between causes (practices) and effects (outcomes) determine what type of problem domain we are in and how we operate in that domain. It is therefore critical that we are aware of what type of problem domain we are in so we can respond accordingly as each type of problem domain has a different approach to achieving desirable outcomes.

### Chaos
When we first enter in a problem domain, we tend not to see any patterns. Even in well-known problem domains, the participants and the circumstances may have changed sufficiently to make the problem domain unrecognizable, at least, initially.

When in a chaotic problem domain, our first priority is to act to change our situation. Failure to act results in failure to change. Our goal is to move into a more predictable situation,

If we take some action, we may not see what effect it has. This is most often due to not knowing what to observe. In a chaotic problem domain, cause and effect are unclear. We do not yet know what to monitor to sense our situation.

When in the chaotic problem domain, we try something and see how it affects our domain. These **Novel Practices** are new and untested, but once tried, we sense their effect on our domain and respond with additional new practices until we begin to see patterns. We begin categorizing these Novel Practices into those that result in desirable outcomes and those resulting in undesirable. In this stage, we are simply acting and then sensing what the results are responding accordingly.

Once we begin to see patterns and indications of cause and effect, we enter a new type of problem domain; complex.

### Complex
In complex problem domains, we take the Novel Practices with positive outcomes and evolve them into more effective, **Emergent Practices**. We still do not know what we don't know, but we are performing experiments based on what we observe. We probe the domain, sense its state, and respond accordingly.

In complex problem domains, our actions change the situation in unpredictable ways. The relationships between cause and effect are still unknown, but they are becoming clearer. Once those relationships become reproducible, we enter the next type of problem domain; complicated.

### Complicated
In complicated problem domains, the relationship between cause and effect requires analysis or expertise and we rely on experience to guide us to desirable outcomes. This is because there are a range of right answers that bring varying degrees of success.

This is where **Good Practices** are used because we know from experience that there are practices that will result in positive outcomes.

Software development is an example of a complicated problem domain. There are many right ways to do things and it requires experience to know what practices will be most efficient in achieving the desired outcomes in the current environment.

### Clear
In Clear or simple problem domains, the relationship between cause and effect is clear: if you do X, you will get Y. This means that there are rules in place to achieve desirable outcomes. 

This is the domain of **Best Practices**, standard operating procedures and practices that have been proven to work to achieve consistent results. In this problem domain, one finds the proper rule and applies it.

The challenge we often have is not all problem domains have clear and consistent cause-and-effect relationships. There are too many variables in most problem domains to manage effectively. It is not easy to identify best practices for all problem domains.

## Applying Practices
Initially, we are in a state of confusion. We do not know what type of problem domain we are in, the goal is to move into a domain where we can apply practices to achieve the desired outcomes. This is easiest in the Clear or simple domain where we can apply Best Practices to achieve desired outcomes consistently, but not all problem domains have consistent cause-and-effect relationships. Sometimes the best we can do is move our problem domain to a Complicated domain and rely on on experts to guide us to desirable outcomes.

As we manage our situation from confusion to chaos, we begin experimenting with **Novel Practices**. We act first then sense the response to our actions to determine our next response. After enough iterations of "act-sense-respond," we begin to spot cause-effect relationships and gradually move into the complex problem domain.

As we move from chaos to complex, we probe our environment to sense our situation and respond with **Emergent Practices** that are evolving with our understanding of the problem domain. We continue this "probe-sense-response" cycle until we identify more consistent cause-effect relationships and gradually move into the Complicated domain.

As we move our problem domain from complex to complicated, we sense our situation, analyze what **Good Practices** we can apply, and respond with a known practice to achieve an expected result. It is through experience and expertise that we continually apply known practices to achieve an expected result. We cycle through multiple iterations of "sense-analyze-respond" until we find a consistent mapping of practices that achieve consistent desirable outcomes and move our problem domain into the Clear domain.

As we move our problem domain from Complicated to Clear, we begin to identify **Best Practices** that can be used to achieve desired outcomes. In Clear or simple problem domains, there is a clear mapping of a known practice to a known outcome. It then becomes a matter of sensing the situation, categorizing the situation, and responding with a known best practice. The cycle of "sense-categorize-respond" results in consistent desirable outcomes.

## Complacency
Once a problem domain is successfully moved into the Clear domain, is it easy to become complacent. Problem domains do not remain constant. It is easy for a problem domain to move quickly from Clear to Chaotic, particularly in technical and business domains. 

Management must always reassess their problem domain and look for inconsistencies indicating practices (causes) require updating to take into account changing environmental factors. Failure to respond quickly to changing problem domains will result in undesirable outcomes moving the domain into chaos.

Most commonly, a Clear problem domain may shift into a Complicated domain when a new factor is introduced. Consider a manufacturer that must deal with a new competitor. The practices that worked for the manufacturer in the market before may not work with new competition. Management must determine what new practices must be created to achieve the desired outcomes. Good practices like improving customer service may address the issue. 

Sometimes a changing problem domain requires Novel/New practices to move the problem domain into more consistent outcomes. A product may require redesign to meet market expectations, customer service may need to offer new services to maintain customer satisfaction. A new competitor or technology can quickly turn a long-time Clear domain into Chaos overnight and management needs strategies to respond.

It should be noted that all domains can change. Just when you think you have a set of **Good Practices** for a **Complicated** domain, an external factor can send your problem domain into chaos. What used to be considered good practices in data processing no longer apply in today's technology environment. Virtual Machines used to be considered good practices, but with that wide acceptance of containerization, VMs are no longer considered a good practice.

## Review
Finding and applying the appropriate practice depends on the type of problem domain you are in.

All problem domains start out in a state of confusion, and progress through at least four basic states:

- **Chaotic**
  - Unknown or decoupled cause-effect relationships - act or fail
  - Strategy: act-sense-respond
  - Novel Practices
- **Complex**
  - Loosely-coupled cause-effect relationships - experimentation
  - Strategy: probe-sense-respond
  - Emergent Practices
- **Complicated**
  - Known cause-effect relationships - requires expertise
  - Strategy: sense-analyze-respond
  - Good Practices
- **Clear**
  - Tightly-coupled cause-effect relationships - 
  - Strategy: sense-categorize-respond
  - Best Practices

Complacency - No problem domain is static. Change is inevitable and it can occur gradually or overnight. Management must continually assess their problem domain and apply the appropriate strategy to achieve desired outcomes.

