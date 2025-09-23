---
title: "Assembler Honors Contract"
author: "John Salata"
description: "One of my most memorable Honor's Experiences was independently creating a complex system"
date: 2025-09-23T10:25:19-05:00
draft: true
toc: true
---

One of the most challenging and rewarding Honor's Experiences I completed was my Honors Contract for CSCI-C 335: Computer Structures.

The entire class focused on learning how computers work at an extremely low level. We discussed how different components of a processor work and how simple parts can be combined to enable complex behavior.

The semester-long project that everyone in the class completed was to apply our knowledge and build an assembler that would work using the hypothetical processor our class centered around. Everyone would be split up into teams and split up the work in order to make it a bit easier to work on.

However, as mine was an Honors Contract, I had the opportunity to complete this project by myself. This introduced a few challenges as I would be taking on more responsibility than my classmates.

## Challenges

For starters, I had to hold myself accountable. Building an assembler from scratch is not easy and requires a lot of planning and understanding of the core components. I recently completed a course about software design patterns and saw this as the perfect opportunity to apply what I learned in a new way.

Part of the problem with trying to plan a project like this is that you have to understand what exactly it is that you are building. Every time I would draft up a solution, I would learn about a new feature that we would have to add that would require significant reworking to the overall design. In hindsight, the patterns I was trying to implement did not match up with what they should have been doing.

Eventually, I created a design that would theoretically work and slowly implemented each feature one by one. Test driven development (TDD) was critical to making sure that each new addition didn't break a feature somewhere else. Frequently small changes would have large consequences and frequent testing helped me identify problems before they were permanent.

## Structure and Presentation

Below is part of the diagram that would model how parts of the assembler would work.

![Assembler Diagram](/diagram.png)

Here is the final project PowerPoint that helps to explain parts of the overall structure. Since it was for a Computer Science class, I kept the default theme as it is clean, simple, and used by nearly all of my professors.

![Assembler PowerPoint](/FinalProject.pdf)

For more technical details, I highly recommend reading the full project page [here](/projects/assembler) and checking out the technical documentation [here](/docs/apidocs/index.html). Source Code can be found on my GitHub [here](https://github.com/jrsalata/assembler) as well.
