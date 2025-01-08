---
date: 2019-01-19
title: Project X
linkTitle: Project X
description: >
  A coworker handed this to me many years back when we were conducting technical 
  interviews for developers and asked if I could guess what the output would be.
author: Steve Cote ([@sdcote.com](https://bsky.app/profile/sdcote.com))
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---

One of the lead developers and I were conducting interviews for new developers at a technology start-up and he came across a humorous example of a Java program when researching technical questions to ask potential candidates. He asked if I could tell him what the output of this simple Java. I could not by just looking at it. Maybe you can:

```java
class X {
  int X;
  X(int X) { this(X, X++); this.X = X; }
  X(int X, int XX) { this.X += XX += this.X + X++; }
  int X(int X) { X(this); return X; }
  X X(X X) { X.X += ++x.XX; return new X(X.X); }
}

public class x {
  static int XX;
  static int X(X X) { return X.X; }
  public static void X(int X) { System.out.println(X); }
  public static void main(String[] XXX) {
    X X = new X((new X(++x.XX)).X);
    X(X.X(X.X));
    X(X.X(X).X);
    X(X(X.X(X)));
  }
}
```

## Code Readability
I post this primarily because I see examples of unreadable code almost daily at client sites. The reasons for such code are many. Some cut and paste code fragments they don't fully understand, others modify code fragments to fix some bug only to leave the entire method or class a confusing mix of naming, formatting, and styles. Others like to show how skillful they are by doing everything in the fewest lines of code possible.

Writing readable code is crucial for many reasons, and it benefits developers at all levels, from entry-level junior coders to senior developers. 

### Collaboration
First and foremost, readable code enhances collaboration. In a team environment, multiple developers often work on the same codebase. When code is written clearly and consistently, it becomes easier for team members to understand, review, and contribute to the project. This reduces the likelihood of misunderstandings and errors, leading to more efficient and effective teamwork. I have been on teams where only one developer could be assigned a backlog item because only that developer understood the code. This always resulted in a throughput issue for the team. When another developer did try to add a feature or fix a bug, they spent crucial time trying to understand the code and "figure out what it was doing." This adversely affected the entire team.

### Efficiency
Readable code simplifies maintenance and debugging. Code that is easy to read and understand allows developers to quickly identify and fix issues. This is particularly important in large projects where the original author of the code may not always be available to explain their logic. Clear code with meaningful variable names, comments, and a logical structure helps developers, regardless of their experience level, to navigate and modify the code with confidence.

### Knowledge Transfer
Writing readable code fosters better learning and knowledge transfer. Junior developers can learn best practices and coding standards by reading and understanding well-written code. This not only helps them improve their skills but also ensures that they can contribute more effectively to the team. For senior developers, readable code allows them to mentor junior team members more efficiently, as they can easily explain the code's functionality and logic.

An important case for knowledge transfer is when the Testing Team tries to create tests. They need to be able to easily read and understand the code so they can create appropriate unit and integration tests. While this should be the responsibility of the developers, most real-world scenarios involve testers being brought in after the code is in production to improve product quality and to leave the developers to focus on the backlog. While this is not the best scenario, it is a fairly common practice. Testers tend to be most capable of creating tests in their framework of choice and not necessarily expert coders well-versed in multiple languages. The longer it takes the testers to understand the code base the longer it takes to create tests for it.

### Cost
The time it takes to onboard a team member costs time and money. If you are adding a new member to a team, the time they take to learn the codebase is time they are not generating value for the customer. Even when temporarily adding a team member, the time it takes them to understand the codebase is only costing money with no return on that investment.

Time spent in learning the codebase is seldom regained. The codebase evolves with each backlog item and learning convoluted code can be lost when that code changes. 

Consultants normally charge by the hour and the more difficult the code base is to read and understand, the more the client is charged before the consultant can start producing value. 

Over the years, I have seen many examples of difficult-to-read code thrown out because it cost far more to maintain than it provided in value. And in almost every case, the developer responsible for the code gained more infamy than respect. See some bad code? Just use `git blame` and see who is responsible.

## Summary

Writing readable code is essential for collaboration, maintenance, debugging, learning, and cost avoidance. It ensures that code is accessible and understandable to all developers, regardless of their experience level, ultimately leading to more successful and sustainable software projects.

BTW - The output of the above code is 3, 9, and 13 each on separate lines.
