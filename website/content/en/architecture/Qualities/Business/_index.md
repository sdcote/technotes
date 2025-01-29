---
title: Business Qualities
description: There are qualities in addition to those that apply directly to a system and are equally important in shaping a system’s architecture. They are concerned with issues such as cost and schedule, marketability, and organizational factors such as workforce availability.
weight: 4
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}


- **Cost** - Development Budget
- **Legacy System Dependence** - The system's ability to be integrated with (existing) systems.
- **Projected Life** - Prototype vs. Utility vs. Infrastructure systems
- **Release Schedule** - Base functionality vs. full-featured release.
- **Targeted Market** - Mass Market vs. Targeted Computing Environment.
- **Time to Market** - Build versus Buy versus Reuse.

## Cost

The development effort will naturally have a budget that must not be exceeded.  Different architectures will yield different development costs; for instance, an architecture that relies on technology or expertise that is not resident within the development organization will be more expensive to realize than one that takes advantage of assets already in-house.

## Legacy System Dependence

If the new system must integrate with existing systems, appropriate integration mechanisms must be defined. The architectural constraints implied by this integration must be analyzed for potential effects on cost and schedule.

## Projected Life

Modifiability and portability across different platforms become essential if the system is intended to have a long lifetime.  However, building in the additional infrastructure (such as a portability layer) to support modifiability and portability will usually compromise time to market.  On the other hand, a modifiable, extensible product is more likely to survive longer in the marketplace, extending its lifetime.

Projected life influences trade-off decisions. Long-lived systems tend to require longer times to market and larger budgets.

## Release Schedule

Short release schedules imply a base function initial release that emphasizes modifiability, as opposed to a full-featured release that is not intended to be evolved much over its lifetime.

## Targeted Market

Mass market deployment emphasizes the qualities of Portability and Functionality (full-featured vs. incremental)

## Time to market

If there is competitive pressure or a short window of opportunity for a system or product, development time becomes important. This, in turn, leads to pressure to buy or otherwise reuse existing components. Time to market is often reduced by using prebuilt components such as commercial off-the-shelf (COTS) products or components reused from previous projects. The ability to insert a component into a system depends on the decomposition of the system into components, one or more of which are prebuilt.

