---
date: 2018-12-12
title: Why You Should Use UML
linkTitle: Why You Should Use UML
description: >
  Unified Modeling Language (UML) is very much just that, a language. UML is a 
  visual language for representing complex concepts. It removes ambiguity from 
  technical illustrations and provides clear representations of design elements. 
  If you want to greatly improve your technical communication skills, start using 
  UML in your diagrams.
author: Steve Cote ([@sdcote.com](https://bsky.app/profile/sdcote.com))
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---

Communication is absolutely critical to success in any endeavor. This is especially true in business where time is limited and often very expensive. Technology projects involve an enormous amount of communication and the ability to effectively communicate complicated ideas is critical to success. Diagrams and illustrations are used to convey large amounts of information with relatively few artifacts.

Most are familiar with the old adage "A picture is worth a thousand words," but in today's business world, some diagrams result in "a thousand questions." Confusing diagrams, which are hard to interpret, waste time, result in errors, and even mislead.

To make visual communications more efficient in the complex world of software development, the unified modeling language was created to establish a set of common notations to foster a common understanding between different development teams and stakeholders.

## What is the Unified Modeling Language (UML)?

The Object Management Group (OMG) UML specification calls it "a standard way to write a system's blueprints." Physical engineers have standard diagramming languages to illustrate the structure, plumbing, and wiring in a building, and software engineers have UML. It is a standard visual vocabulary which allows for the clear, unambiguous representation of a systems design.

UML is a collection of graphic notations and common terminology that can be applied to the domain of software engineering with the goal of enabling teams to illustrate sophisticated systems without requiring esoteric or tribal knowledge on the part of the reader.

## Why Should I Use UML?

UML is beneficial for many reasons and is worth consideration regardless of a team's methodology and practices. If you need to communicate, UML can help.

### Standard

UML is a well-accepted, standard way to represent complex concepts. UML is the current [OMG standard](https://www.omg.org/spec/UML/About-UML/) for programming in object-oriented programming languages and as a standard, it is widely understood. This makes it easy for a new programmer to step into a project and be productive from day one. Using a standardized modeling approach removes the guesswork from reading technical documentation. An arrow on a diagram has a very specific meaning in UML and the viewer will be able to understand exactly what is represented by that arrow.

### Efficient Communication

A UML diagram is beneficial in that it is very readable and provides an efficient way to communicate complex concepts.

There are some who would argue that the code is the only true source of documentation of the system, and while it is the one true source of truth, there are some problems with using the code as documentation. First, it is unreasonable to expect someone to go through the entire codebase to understand the system. This would require special knowledge and many hours of effort. Scanning the codebase is also very inefficient and it is easy to miss broad behavioral aspects of the system. Secondly, the source code only describes part of the system and nothing about runtime structures and infrastructure. Thirdly, the source code is only meaningful to those proficient in that language. Complex systems are often polyglot and require knowledge of several languages and technologies for a meaningful understanding of the codebase.

How many times have you seen an arrow on a diagram and wondered what it represented? Even when explained in one diagram, an arrow on the next diagram often represented another concept. I have seen an arrow represent the direction of information flow on one page and on the next, it represented a reference. Then on the third diagram, it represented a dependency. Each one of these diagrams required explanation and could not be interpreted without assistance. UML allows everyone to use the same visual language when diagramming concepts. No explanations are necessary and all your documents gain uniformity.

### Stakeholder Confidence

Many stakeholders have limited technical understanding. As a visual representation of complex systems, UML provides a way to illustrate the structure and behavior of the system in a way that is easy for readers of many levels of technical understanding. When project stakeholders see UML, they know the project team is following accepted standards and practices. It is clear the technical team is not "winging it" or just "putting something together." UML diagrams show the technical team is educated and following proven standards.

UML has been successful in helping bridge the gap in communication between technical and non-technical project members for many years. Teams that use UML build stakeholder confidence in that stakeholders have a better understanding of the technical details involved in the project. Most CTOs will be able to discern the correct meaning from UML diagrams with little explanation. Project managers can understand UML sequence diagrams with little training. And because UML is a standard, what they learn on one project will help them with the other technical projects in which they participate.

Admit it. When you see documents with clip art, you immediately discount the author's message. The same thing happens when readers look at your diagrams and see the same old Visio shapes or simple box and line diagrams. Knowing and using UML not only improves your communication, but it also conveys an image of professionalism to your reader.

### Technology-Independent

UML is useful for describing designs regardless of the programming language used. It also is as useful in operations as it is in programming. UML helps describe cloud architecture and design regardless of what cloud platform is being used.

Vendors have a tendency to create new visual languages for their products. Amazon cloud diagrams look different from Google and Azure diagrams. It is almost as if the marketing departments of these platforms created diagramming languages for their respective platforms to help more with branding than functionality. The result is little more than icons and logos connected with ambiguous lines. That might be nice for slide decks, but nowhere near the information density of UML.

It is possible to create a Deployment Diagram, for example, which can be applied to any of the cloud platforms, meaning you can design a system without influencing the choice of technologies until a proper trade-off analysis has been performed. This is important as how a system is represented can unduly influence technical decisions.

UML allows everyone to focus on the design and not the technology.

### Planning and Prototyping

UML helps to plan a program before the programming takes place. Tome tools will take a UML model and generate code in any of several languages. Granted, this requires relatively detailed class models, but this can help reduce overhead during the start-up stage of a system. UML models are easy to change and can allow the regeneration of a section of code whereas reprogramming can be tedious, time-consuming, and error-prone. Some tools also read in code and generate UML models allowing for round-trip engineering of code. I have personally been involved in a project that read in C++ code and generated a Java project that saved months of porting effort.

### Durability

The UML standard has been around for decades and it is possible to pick up a UML diagram from 20 years ago and completely understand it. There is no need for the author to explain what the boxes represent and how the lines should be interpreted.

## Debunking UML Myths

UML has received its share of bad press. Just like any tool, UML can be misused and taken to ridiculous extremes. This has created many UML opponents and promoted quite a bit of misinformation about UML.

### You Need Software To Benefit From UML

UML is a visual language and any time a diagram is necessary, UML keeps the vocabulary uniform and consistent. Anytime you create a diagram, you can use UML notation. It is not necessary to use software to generate UML diagrams. A vast majority of the UML I have used was on whiteboards and on paper. No software was necessary to clearly illustrate the complex ideas in those meetings.

The best modeling tools are any drawing surface. [Whiteboards](https://amzn.to/2PzFfZU), flipcharts, papers, and windows (with dry-erase markers) are where UML is used, not just in Computer Aided Software Engineering (CASE) tools or Microsoft Visio. Remember that UML is a uniform way of illustrating concepts and while many diagramming applications support UML, they are not required to benefit from understanding this visual language of design.

If your team does use a CASE tool, you will find a whole new level of productivity. All your UML diagrams will make perfect sense in the new tool. The tools output will make sense to the team. This is because both you and the tool will be using the same vocabulary. The learning curve for the software is reduced and you can achieve benefits with the tool faster.

### UML Is Just For Object-Oriented Design

While it is true that UML has evolved over the years to model object-oriented systems, the current specifications allow it to be extended in ways that allow it to be used for nearly any systems design.

If you ask seasoned software professionals about UML, they often describe it as a tool to perform object-oriented analysis and design (OOAD). True, UML has proven to be very popular in supporting OOAD activities, but UML has the features to make it valuable in other practices and software development approaches.

### UML is Related to Waterfall Practices

The unified modeling language is a vocabulary and set of notations, not practice. Agile teams have been using UML for years and it is often the go-to standard for helping teams decompose complex concepts (during whiteboard sessions) into smaller elements so epics and features can be incrementally addressed in multiple iterations.

UML has been in wide use since the late '90s and this has led many to believe that UML is a characteristic of big up-front design (BUFD). Anyone who has been in systems design for large companies will probably have seen UML diagrams in thick requirements documents that were created in traditional waterfall design methodologies. This is unfortunate, as UML was never intended to imply design practices, only standardizing the visual language of systems design.

Many teams practicing agile methodologies use UML daily. It is a way to quickly and clearly diagram complex concepts so the team can spend less time discussing the interpretation of a diagram and more time delivering value. UML streamlines communications and makes whiteboarding sessions run faster.

UML diagrams can be very information-dense, making them great for big visual representations of design principles for the team to follow. Every iteration planning session can refer to the one architecture diagram to make sure design decisions stay on track. As the code is being written, it can be mapped to the guiding architecture diagram. If the code does not seem to fit anywhere, a quick change to the code or the architecture can be performed to make sure everyone involved is heading in the same technical direction.

UML can span teams and make scaling agile practices easier because less time is spent in meetings explaining diagrams and asking "discovery" questions. Concepts are clearly communicated and meetings are shorter.

There is also a practice known as Agile Modeling which leverages the information density and uniformity of UML with other modeling practices. The use of UML in agile practices makes everyone more efficient.

### UML Is Too Difficult To Learn

Many developers will not take the few minutes it takes to learn the basics of UML. The [UML specification](https://www.omg.org/spec/UML/About-UML/) is long and difficult to read. UML 2.5.1 is around 750 pages (but, at least there are a lot of pictures). The fact the specification is so big and complex prevents many people from even starting.

If you think about what your diagramming needs are, you will probably only need four basic concepts:

1. How to depict an element (class or component)
2. How to depict an interface
3. How to associate elements
4. Grouping (classifiers)

It is not necessary to learn the entire specification to start achieving the benefits of a standard. Just like any technology, learn only what you need. As your needs change, learn more. Just remember not to use UML idioms the reader may not know. Keep your diagrams simple.

There are analysts whose job it is to create documentation and many have been using UML for years. Their experience in creating technical diagrams has allowed them to learn and use many obscure parts of the UML specification. These people pride themselves in their documentation expertise and can create diagrams that boggle the mind. Most of us do not need diagrams as complex as those the documentation professionals create. Complex diagrams are often a hindrance to communication. If the reader cannot understand your diagram without knowing a 750-page specification, using a standard is no better than an informal or proprietary diagram.

If your diagrams are too confusing to be understood, you are doing it wrong. Keep things simple and easy to read. You don't have to use every feature of UML to be a better communicator.

## Summary

The Unified Modeling Language is often misunderstood as a throwback to waterfall methodologies and big up-front design. The truth is UML is a standard way to visually represent complex systems so everyone can focus on the design and not the interpretation of the diagram. The benefits of UML include the following:

- Industry-standard way of representing complex systems
- Improves communication
- Simple to learn (use only what you need)
- Technology independent
- Widely recognized

There are many great ways to start learning UML, and in a matter of minutes, you can begin to create diagrams with improved readability and reader acceptance.
