---
title: "Development Growth"
author: "John Salata"
description: "A reflection on a few different projects and my growth from them"
date: 2025-10-21T10:25:19-05:00
draft: false
weight: 3
toc: true
---

In my time at IUPUI and IU Indianapolis, I was able to apply the general skills that I gained into many different class projects, personal projects, and professional work as well. Looking back from my freshman year, I've made some practical projects that solve real problems in ways that helped me tremendously. Here are just a few that I've worked on and how I grew from them.

# Crowdcam Capstone

In the Spring of 2025, I took a capstone course where we completed a group project. We could use any framework or tools we wanted as long as we made a viable product that could be used in the real world. 

The result of that project was [Crowdcam](https://github.com/crowdcam/crowdcam): A crowd sourcing media platform. It allows people to create events where anyone attending can submit media to share. It also requires media to be approved in order to be public to ensure only moderator-approved content can be seen by the public.

## Inspiration

When our small group was brainstorming ideas, there were a few different directions that we wanted to take. But very few of them were original or new. We wanted to build something that could have a real-world purpose at the end of the day. Thats when I introduced a real-world problem I faced in the summer of 2024.

In 2024, I served as the Studio Boulder Program Lead for the 2024 National Order of the Arrow Conference (NOAC). NOAC is essentially a week-long conference for Scouting America's National Honor Society: The Order of the Arrow (OA). 

In this role specifically, I would be leading the Studio program for this conference. The Studio program allows participants to submit photos and videos to our team where they can then be published online to show the Conference from their point of view. Afterall, our photography team is relatively small and we can not capture every moment that is worth sharing.

The biggest challenge in this role is the sheer amount of media that we collect. With over 6000 pieces of media and 400+ participants, keeping track of everything was difficult. Not only did we have to organize the files by who submitted them, but we had to sort and cull in order to find the ones that were actually usable.

This problem is what inspired the creation of Crowdcam. We needed a platform with moderation tools and automatic sorting of submitters. We saw great potential in this idea and many ways to expand it so it can be used by many different people.

## Implementation

For this project, we decided to use the Django framework. It is based on Python and has many powerful features built in that we would frequently use. The less we had to build from scratch, the better off we were. 

None of us were familiar with Django so it presented us with the opportunity to learn. The documentation was great and we were able to use the concepts we learned in previous classes and apply them here.

## Documentation and Planning

While there are comments in the code to describe the goals and purpose of specific components, this was the first time that we had to create software requirement specification docs and plan in-depth what we were going to do. This was more challenging than it sounded like since we never worked on a project where the requirements and design were completely up to us. We all had different ideas for what we wanted to see and had to work together and make a plan that integrated everything smoothly. It also did not help that none of us enjoyed working on front-end design and so our user interfaces could be refined significantly.

Our original architecture was a bit off since Django works differently than we originally expected and found easier ways to fulfill our requirements. This was the hard part about using a framework no one was familiar with. It was a true trial by fire and I enjoyed it. At the end of the day, we created a working prototype that with a few more refinements could be used today.

# DuesManager Automation

Note: I wrote a more in-depth article about this project [here](/projects/duesmanager). It contains some more technical details whereas this is a brief overview.

A common theme with DuesManager and Crowdcam is that they started off as solving problems that I encountered with my work in Scouting. To be honest, I have a hard time being motivated to do personal projects so I pick projects that have a purpose and solve a problem. DuesManager is no different.

## Problem

In my local Order of the Arrow Lodge, we have a payment portal and a member portal that handles all of the data and payments within the Lodge. In order to log dues payments from the payment portal, an adult volunteer has to go in and manually mark the dues payments on our member portal. This is a slow and inefficient process that takes up valuable volunteer time.

## Solution

One of the certificates I've earned at IU Indianapolis is in Cognitive Automation which is a fancy way of saying that I learned how to use automation tools with AI to complete complex tasks. Most of the time, these are repetitive tasks that are tedious for humans to do and have no way to implement a solution with traditional programatic tools.

The end result ended up being a powerful task that would find the dues payments on the payment portal, process them through a python script to clean the data, then import the results on the members portal. Final results and any anomolies would be sent to a Slack channel for further review.

I also created a Slack Bot so this process can be ran at any time by certain members in our Slack Workspace. 

## Results

The end result is that we have an automated process with a low failure rate that saves us hours per week. Up to date data empowers our youth to make more informed decisions with their program and engagement strategies. We also identified additional processes that can be automated in the future so we can continue to save time and have up to date data to work with.

From a personal perspective, I refined my automation skills by working with a real-world problem that has a real impact on an organization. While I have much to learn in this field, the experience was extremely valuable and I recognize the areas in which I can grow in the future.

# Software Engineering Internship at Resultant

In the Summer of 2025, I had the opportunity to work at a mid-size consulting firm based in Indianapolis called Resultant. To say that I learned a lot and made a recognizeable impact in my short time there would be an understatement. Not only did I apply the technical skills I gained from IU Indy, but I learned about the complex world of consulting and the importance of being client-focused. It was a great opportunity to work with some amazing people over the summer.

## Cloud Migration Project

After I completed all of the routine onboarding trainings and meetings, I was handed my first big project on the third day: migrate services for affordability on Google Cloud Platform (GCP). I worked with another software engineering intern named Phoebe on this project and neither of us had any direct experience with GCP or the services we were working with. Our managers gave us the goal of "make it as cheap as possible" and no further instructions.  They let us ask questions throughout the project and let us pick our own direction. They handed us the keys to the platform and let us wander and explore on our own.

In hindsight, the amount of independence and freedom that they gave us was the best thing. Phoebe and I spent hours investigating the current configuration. Trying to decipher what was going on was more educational than being handed instructions on what to do and how to do it. There were also some considerable configurations that made Phoebe and I both ask "what could possibly be the reason for xyz?". 

I spent hours researching different services, prices, and tradeoffs to fit our requirements. We created a formal(ish) proposal that was approved. 

Naturally, our plan changed as we discovered new issues and had to adapt. Multiple parts of the migration were more difficult than we originally expected and needed additional care to ensure that they would run properly.

### Migration Results

At the end of our migration, we brought costs down from $220/day down to <$2/day or around $80,000/year to just around $300/year. The services we migrated have the same availability and redundancy as they did previously.

Once again, Phoebe and I had no prior experience working with GCP or any of the services that we had to move internally. We learned, adapted, and applied what we knew. No one directly told us to take the path that we did. We discovered it on our own. That made it much more exciting and educational to work on.

## Exhibitors Corner

After we completed this migration project, our next task was to work on a program called Exhibitors Corner. Two different clients use this program to manage their fairs and festivals. The program itself has a reputation for being old, difficult to work with, and messy in some areas.

On the technical side, Exhibitors Corner is almost 10 years old and was developed using Ruby on Rails. I had no experience with Ruby on Rails before working on this project. Despite that, I was able to contribute significantly to the development and created features that were valuable to the clients.

The first few weeks working on this, I was handed small bugs and issues that needed to be fixed. This gave me an opportunity to become familiar with the project and how it worked internally. The concepts I learned while working on Crowdcam were the same. This made it easier to work on and learn this new system.

After going through their backlog of issues to work on, I was handed more complex features to work on. In a way, I was treated not as an intern, but as a full-time developer with responsibilities, and some light deadlines. I was a member of a wonderful team that I can not speak highly enough.

I also learned how important it is to effectively communicate with project managers and other developers. There were multiple times where I made sure I understood the end goal and motivation of the client so my implementation would be what the client needed and not what they thought they wanted. There is a difference and it greatly matters. 

### Sorting Page

One of my most significant contributions was done almost on accident. The problem I was given was a page tended to "jump" up and down when editing multiple items at a time. It was recommended to me to implement a filtering page so there would be less items and less lag overall.

The problem and solution seemed obvious to me at the time. I spent a few days working on the filtering page and fixed some additional issues along the way. When I was finished, I tested my work and found that the page still jumped occasionally.

Weird? If the issue was caused by too many entries, it should not be happening with this few entries.

And then I found it. The _actual_ cause of the page jumping. A CSS tag was being removed after a certain period of time which caused the jupming effect that was so bothersome. A simple 3 line change is all that was needed to fix the issue. 

Despite this, the client was intrigued by the filtering page. I presented it to them and they loved it. I was able to solve the problem and create a complex feature that was needed for their use case. 

# Reflection

With all of my experiences, I know that I have much to learn. How exciting?

I know enough to be able to quickly learn and adapt to almost any problem. My passion truly is solving problems with people so they are better equiped to make the world a better place.

I also think that what made some of these experiences stand out was not my technical abilities. What stood out to me was the way in which I interacted with those I worked with. I am a ambitious, innovative, and passionate person that loves using my technical skills to solve problems.