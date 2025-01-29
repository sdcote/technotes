---
title: Runtime Qualities
description: There are qualities that can be observed and measured as the system executes.
weight: 2
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

- **Availability** - A Measure of the time the system is up and running.
- **Functionality** - Ability of the system to do the intended work.
- **Performance** - Responsiveness to stimuli (requests & events).
- **Security** (Confidentiality, Integrity & Availability) - Resistance to unauthorized use, denial of service, or data corruption. 
- **Usability** - Efficiency, Learnability, Satisfaction, Error Avoidance/Detection.

## Availability

Availability measures the proportion of time the system is up and running. 
It is measured by the length of time between failures as well as by how quickly the system can resume operation in the event of failure. The steady-state availability of a system is the proportion of time that the system is functioning correctly and is typically seen as follows: 

>    time to failure/(time to failure + time to repair) 

Availability comes from both "time to failure" and "time to repair"; both are addressed through architectural means. 

## Functionality

Functionality is the ability of the system to do the work for which it was intended. 

Performing a task requires that many or most of the system's components work in a coordinated manner to complete the job, just as framers, electricians, plumbers, drywall hangers, painters, and finish carpenters all come together to build a house cooperatively. 

Therefore, if the components have not been assigned the correct responsibilities or have not been endowed with the proper facilities for coordinating with other elements (so that, for instance, they know when it is time for them to begin their portion of the task), the system will be unable to perform the required functionality. 

## Performance

Performance refers to the system's responsiveness − the 'time required to respond to stimuli (events) or the number of events processed in some interval. 

Performance qualities are often expressed by the number of transactions per unit of time or by the amount of time it takes a transaction with the system to complete. 

Since communication usually takes longer than computation, performance is often a function of the amount of communication and interaction between the system's components, which is clearly an architectural issue. 

## Security

Security is a measure of the system’s ability to resist unauthorized attempts at usage and denial of service, while still providing its services to legitimate users.  Security is categorized in terms of the types of threats that might be made to the system and includes the following.
- **Denial of service:** This form of attack prevents a targeted system from providing, receiving, or responding to network services. It typically occurs by flooding the target with connection requests or queries.
- **Assuming trusted identity:**  This attack attempts to gain access to the target by assuming a false identity. The identity can be that of a host trusted by the target or of a user known to the target.
- **Theft of privileged data:**  This attack attempts to gain access to data on the target system, either a password for future attacks or privileged data. The data being stolen can either reside on a target machine or be in transit between one machine and another over a network.

## Usability

Usability is the system's ease of use and training of the end users.  Usability can be broken down into the following areas.

- **Learnability**:  How quick and easy is it for a user to learn to use the system’s interface?
- **Efficiency:**  Does the system respond with appropriate speed to a user’s requests?
- **Affect/Control:**  Does the user feel good about using the system?  Does the system make the user’s job easier?
- **Error Avoidance and Handling/Helpfulness**:  Does the system anticipate and prevent common user errors?   Does the system communicate well and assist the user in resolving problems?
- **Control**:  Does the user feel that the software responds consistently?



