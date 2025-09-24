---
title: "Challenges"
date: 2024-12-10T20:02:55-05:00
draft: false
weight: 2
author: "John Salata"
description: "A brief reflection about the various challenges I overcame in this project"
toc: true
---

## Tracking
I heavily relied on GitHub issues to help me keep track of every requirement and step that was needed. There were also a few times that a rewrite or refactor was needed in order to implement a given feature. As of writing this report, there were [34 total issues](https://github.com/sheepman39/Assembler/issues) that included new features and improved old ones.

## Building
In the first week or so of the project, I was relying on makefiles to help me compile and run each of my files. However, I quickly realized that would not scale easily as I added more and more complexity. I started to use maven to help me manage the building and testing of this project. I also used a code analysis tool called Sonarcloud that would detect issues that are more language specific and helped me follow best practices. 

## Debugging
When implementing the assembly method for the extended statement, there were a lot of issues trying to figure out why exactly a certain value was calculated. My tests were failing since the generated code did not match up with what was provided by the book. 

It was a strange issue and one that required me to use the java debugger to figure out what was going on. I was able to set different break points and watch the value of different variables to try and figure it out.

Eventually, I discovered that I was miscalculating the displacement and needed to rework how I handled Base relative and PC relative addressing. 

There were many issues like this that required me to use the debugger and track down where an issue was occurring and what exactly was causing it. With each new class or method, the complexity of the project grew. Sometimes, it would be an easy fix. I forgot to set a value in a table or forgot to call a method. Other times, it was difficult to find out where an issue was coming from. Stepping back and coming at the problem from a fresh perspective was helpful. Other times, I would have to do some more research and take it step by step.

## Testing
This was the first project that I used tests to ensure the correctness of my code. In previous projects, I ran a bunch of assertions to ensure it was correct, but never used a proper tool to facilitate it. For this project, I decided to write tests for different classes that had a high potential of failing, such as the Statements, Builders, and Object Writers. 

The most important tests were for the builders and writers. I used the generated object code from the book and compared them against that. If the output matched, it worked. If it didn't match, the test failed and provided feedback on where the difference was. This was extremely important as small changes would have big consequences. One change that fixed a bug would cause a seemingly unrelated feature to break. These tests saved me a lot of time figuring out where an issue could be.

However, there were some issues with my tests. Before I made the builder builder and utility files, I had to manually copy and paste similar logic between different files. One change in one file required all of them to be changed. This was tedious and the odds of me breaking the tests were high. There were times I purposefully changed the output and no failures were reported, which was concerning. I had to ensure that my tests actually worked in order for me to rely on them. 

Overall, it was an insightful time testing and I wish I wrote more tests.
