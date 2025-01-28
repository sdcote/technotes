---
title: Runtime Qualities
description: There are qualities that can be observed and measured as the system executes.
weight: 1
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

- Availability - A Measure of the time system is up and running.
- Functionality - Ability of the system to do work for which it’s intended.
- Performance - Responsiveness to stimuli (requests & events).
- Security (Confidentiality, Integrity & Availability) - Resistance to unauthorized use, denial of service or data corruption. 
- Usability - Efficiency, Learnability, Satisfaction, Error Avoidance/Detection.

Availability measures the proportion of time the system is up and running. 
It is measured by the length of time between failures as well as by how quickly the system is able to resume operation in the event of failure. The steady state availability of a system is the proportion of time that the system is functioning correctly and is typically seen as follows: 
    time to failure/(time to failure + time to repair) 
Availability comes from both "time to failure" and "time to repair"; both are addressed through architectural means. 

Functionality is the ability of the system to do the work for which it was intended. 
Performing a task requires that many or most of the system's components work in a coordinated manner to complete the job, just as framers, electricians, plumbers, drywall hangers, painters, and finish carpenters all come together to cooperatively perform the task of getting a house built. 
Therefore, if the components have not been assigned the correct responsibilities or have not been endowed with the correct facilities for coordinating with other components (so that, for instance, they know when it is time for them to begin their portion of the task), the system will be unable to perform the required functionality. 

Performance refers to the responsiveness of the system − the 'time required to respond to stimuli (events) or the number of events processed in some interval of time. 

Performance qualities are often expressed by the number of transactions per unit time or by the amount of time it takes a transaction with the system to complete. 

Since communication usually takes longer than computation, performance is often a function of how much communication and interaction there is between the components of the system-clearly an architectural issue. 

Security is a measure of the system’s ability to resist unauthorized attempts at usage and denial of service, while still providing its services to legitimate users.  Security is categorized in terms of the types of threats that might be made to the system and include the following.
Denial of service:  This form of attack is aimed at preventing a targeted system from providing, receiving, or responding to network services.  The attack typically occurs by flooding the target with connection requests or queries.

Assuming trusted identity:  This form of attack attempts to gain access to the target by assuming a false identity.  This can be the identity of a host trusted by the target or of a user known to the target.

Theft of privileged data:  This form of attack attempts to gain access to date on the target system, either a password for future attacks or privileged data.  The data being stolen can either be resident on a target machine or in transit between one machine and another over a network.

Usability is the ease of use of the system and of training the end users.  Usability can be broken down into the following areas.
- learnability:  How quick and easy is it for a user to learn to use the system’s interface?
- efficiency:  Does the system respond with appropriate speed to a user’s requests?
- affect/control:  Does the user feel good about using the system?  Does the system make the user’s job easier?
- error avoidance and handling/helpfulness:  Does the system anticipate and prevent common user errors?   Does the system communicate well and assist the user in resolving problems?
- control:  Does the user feel that the software is responding normally and consistently?



