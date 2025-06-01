---
title: "Dues Manager RPA Process"
date: 2025-06-01T00:52:49Z
draft: false
author: "John Salata"
description: "A real world application for robotic process automation (RPA) and integration"
toc: true
---

As a software engineer, I am always looking for ways to be ~~lazy~~ efficient with my work. One of the main reasons why I chose to study this field was my love for solving problems and building a program to solve it for me. Hours of programming can save minutes of work and those minutes of work add up. I made small but powerful scripts that helped me solve problems faster. When I learned how to use a terminal to directly control and operate a computer, it was a dream come true. Tedious tasks that would take hours could now be completed in mere seconds with a simple script. However, there was one area that I could never work with until now: the desktop.  While there certainly are some limited APIs to work with various services, there is no universal interface between everything. The closest universal interface with services that we use every day would be our desktop environment. At the time, I did not know how to programmatically work with the different graphical user interfaces to automate the tasks I did not want to do. Learning about robotic process automation (RPA) changed all of that.

During the last two semesters, I took a series of courses that focused heavily on cognitive automation and RPA. We discussed the ethics, use cases, implementation, and considerations surrounding RPA and other AI-powered automation tools. It was a very eye-opening class that gave me more tools to solve more complex problems than before.

# Problem Description

I do some volunteer work within Scouting as it is an organization that gave a lot to me and I believe it is important to give back however I can. My local Order of the Arrow (Scouting's National Honor Society) Lodge came to me with an interesting problem to solve.

Each year, we collect a dues payment from each member in the Lodge. This payment is recorded on one system that we will call Payment System. We also have our main Member System that handles membership and other domain-specific information. Most of the work the youth and adults do in the Lodge is done within our Member System and can't be integrated with our Payment System. In order to log these payments, someone would go through the Payment System about once a week or so and manually input each payment, receipt number, and total.

Needless to say, this was not an efficient process. It relied on human intervention so data could be out of date, incorrect, or missing. The overall process was repetitive and had clear steps in the decision making process. It was also a time consuming task that needed to be done, but nobody _wanted_ to do. These qualities made it the perfect candidate for automation.

# Initial Steps

As we talked about in class, one of the most important steps when automating a process is to fully understand the process that is being automated. I met with the Lodge Adviser to go over the process and understand the 4 p's: Process, Policies, Procedures, and Protocols. As it turns out, the overall process was a tad more complicated than I first expected it to be. There are many different ways for payments to be made within the system and this changed what we put in our Member System. Each case needed to be considered and covered to ensure accuracy in the system.

## Processing Certain Cases

Given that the Payment System could have its data exported in a CSV file and the Member System can have payments imported from a CSV file, the first thing I tried was a simple export and import from each system. As it turns out, there are some common cases that the export does not account for and would require some processing. This processing could be done in a simple Python Script using various libraries.

This script worked well at combining the input and creating an output file with everything in the proper order. We also added various error files for payments that needed human intervention. The next step was to automate this process so we could automatically download, processes, upload, and report all of the data.

## Process Diagram

Now that I had an idea of the entire process and what would be needed, I made a process diagram to help trace the steps. I knew that I wanted the process to be executed on a routine basis but also wanted a manual trigger accessible to certain people if they needed the most up-to-date information. Since the Lodge uses Slack for most of its communication, I decided that Slack integration would be the most convenient way.

![Process Diagram](https://mermaid.ink/img/pako:eNp1Ul2PmzAQ_CuWn1opiQjkk4c-HKRqpItihbtKB8mDa-8FK2AjY65JQ_57DSQnUalISLvMzA479hUzxQH7-D1Tv1lKtUEv4V4i-5AADYffUB2xFHiVAUcvtDzV6Il0-JMySZRRdmqqQ8v9hEhC6CUHaVB0KQ3kHVyvzoWyDiE1FBmFguhnjcjbF3IxqZIoYloU5uvd_a2TEK0YlKV131amqEyNnjfJBvJfoB-z-4KV1krXaLW7thX6QSXPQN861mrXscKqyASjBmoUkoQ_uiFoPWLlx6HP3ogyp6bJAQWqtP8QRAmzxX_oa_lBM8HROqztmwj-Dy8kLS8mSSwK9F1kcAeC6A507Trstc-bto1eky4KtIMmzrs2eu2R486jPaD7MQUplRKyQ29avc4LrQqb5lo28a52_V22JrWYKMsK6m1yBAlasHYfc35Yby0zJniAc9A5Fdxep2uD7LEV57DHvi051ac93sub5dHKqOgiGfaNrmCAq4Lb8ENBj5rm2H-nWWm_AhdG6U13P9trOsAFlbFS-UNoW-xf8Rn7njeaTybLqess5hPXcSYDfMG-6y1G7nzhzsfj6XS2nM1ntwH-0w5wRkvH88aOO3bGzszxGoVW1TH99D_qZpXOSIPkoANVSYP9iTu7_QWiZP6s?type=png)

# Automation Platforms

In my automation classes, there were two main platforms that we discussed: [Automation Anywhere](https://www.automationanywhere.com/) and [UiPath](https://www.uipath.com/). Each of these platforms provide powerful tools and platforms to create and manage automated processes. I tried using both of them in class and found Automation Anywhere to be easier to use, but tended to lack some of the more advanced integration features in the community edition. On the other hand, UiPath had a steeper learning curve but had many integrations built in and a more generous community license. Since I knew I wanted to integrate other services in the future and be able to run this routinely, UiPath was the obvious choice.

# Building the Automation Process

Before building the process, I decided to list out each step that needed to be done so I had an idea of how complex it would be. The steps are as follows:

1) Log in to the Payment System
2) Navigate to the events page
3) Navigate to the reports page
4) Download the appropriate report
5) Save the downloaded report to the input file of the Python Script
6) Run the python script
7) Log in to the Members System
8) Navigate to the Members Page
9) Click on "Import Dues"
10) Upload the output of the script
11) Copy the output from the Members System
12) Save that output to a new text file
13) Zip all of the relevant input and output files
14) Send it to the previously specified Slack channel

Overall, there is nothing here that is too complex to do for a person. It is a simple and monotonous task. The hard part was ensuring that the script would be reliable and not relying on hard coded data.

I also learned how to safely store credentials in vaults so we can avoid hard coding sensitive data or relying on the autofill in many browsers.

## Integration

Once the process was built, I learned how UiPath Orchestrator worked in order to publish and run it. As it turns out, I needed a computer that could run as an unattended robot so there would be little to no human interference and could be ran 24/7. Given the extremely small scale of this project, I did not need a powerful computer. I just needed something a bit old and power efficient. Thankfully, my family never throws away technology and had an old desktop lying around. Since I can't host it in my college dorm, my parents were kind enough to let me host it in the basement (thanks parents!).

With this desktop set up to run everything autonomously, I created a timed job that would run and report once a week. Realistically, it could have ran every day or hour if we needed to. That may be needed when the number of payments is high, but for now it works perfectly.

## Slack Integration

As previously stated, I also wanted to find a way so other Lodge Admins could run this process with a manual trigger. Since we all use Slack, it seemed like the most obvious solution was to create a Slack Bot.

This Slack Bot would receive a slash command and send a POST request to UiPath Orchestrator. Orchestrator would then add the job in the queue and would be ran. The Slack Bot would run GET requests every 2 seconds or so to receive updates on the job. If something went wrong, it would report it. Otherwise, it would update the timestamp in a message with any other messages that popped up.

This integration made it extremely easy for nontechnical people to utilize the power of automation and process critical data faster and more accurately.

# Results

Overall, this process saves hours of accumulated time for the adult volunteers in the Lodge. This is time that can be spent on working with the youth to reach their goals. Some positions in the Lodge require accurate data on the number of people that paid their dues this year and this automation empowers them to make smarter decisions with accurate and up to date information.

However, this does not mean that it is perfect. Despite my best efforts, we are still finding bizarre edge cases that the system does not currently catch and account for. Thankfully, the error messages that we receive contain plenty of data for us to correct the issue. This process takes significantly less time than the previous method of manually putting the data in. I have a few ideas to try and reduce this process even further, but that will take more time and effort down the road.

Lodge leadership is very impressed and happy with the work that went into this project. This was a personal project that I decided to take on and had no other outside technical help. I greatly appreciate all of the time and insights from the Lodge Admins that helped me understand the processes and entrusted me with this important data.

# Next Steps

Naturally, there are other processes in the Lodge that can and should be automated. This is only a small glimpse as to what is possible with the power of RPA. I already have a small queue of processes that need to be worked on in addition to polishing this one up. I am excited to see how these processes enable us to make smarter decisions with more accurate and accessible data.
