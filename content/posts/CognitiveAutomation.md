---
title: "Cognitive Automation Odyssey"
date: 2024-12-13T14:24:09-05:00
description: "A brief overview of my journey learning about the various aspects Cognitive Automation and Robotic Process Automation tools."
author: "John Salata"
draft: false
toc: true
---

When I first took Social Impact of Bots and Automation, I wasn’t quite sure what exactly Cognitive Automation was. I was more interested in learning new ways to solve problems as that is why I chose to study Computer Science. I love finding problems, breaking them down, and finding new ways to make life easier. Before college, I spent a bit of time writing scripts to automation some tasks and found it pretty fun. I once needed to run a weekly backup of a server and created a bash script to make the backup and email me a log with the details. That little taste of power and convenience is what encourages me to keep learning new skills.

Cognitive Automation, as it turns out, is the type of field I was looking for. It is a relatively new way of approaching problems and automation. As I like to explain in interviews, it is a fancy way of saying that we are using AI to help with automation. We can classify and sort data using computer vision. We can analyze documents to extract key information and input it into the appropriate database. We can automatically process different types of data and find better ways to organize a given business. It is extremely powerful in what it can do.

As part of my Cognitive Automation and Bot Development class, we were able to explore some of these technologies with some traditional and modern tools. It was quite insightful to see what exactly could be done with the right tools and mindset.

The final project in this course was to come up with an idea where we could use RPA and other automation tools to automate a real world task in any industry. The goal was not to build this automation; but rather to come up with the planning and framework needed to implement it in the future. It was important to specify the scope, its feasibility, any ethical considerations, and the tools that would be used.

For me, I used my experience as a teacher’s assistant to help guide me on this project. One of my responsibilities was to grade a few assignments every other week or so. I learned that grading one assignment is not challenging. Grading 50 assignments where everyone has a slightly different style is.

Knowing the challenges of grading, I decided to start there and create a blueprint for a tool that can help automate the grading process and provide clear feedback to students. The overall goal is not to replace graders, but rather to assist them. Any answer that was determined to be very likely to be correct would be marked as correct. Anything else would be flagged for human review. After all, there is a lot of variation and students deserve every opportunity to be marked correctly for the work that they did. Additionally, any incorrect answer could have feedback generated automatically so students know what they need to improve on. By making the overall assessment less tedious for graders, they can focus on providing better feedback to the students and ensure an overall better learning experience.

# Project Challenges

While this was a theoretical project, the technologies and implementations are very much real. It would be easy to wave a hand and say that the entire project can be done with AI and leave it at that. However, there are some important considerations to keep in mind when using AI and RPA to solve problems.

For this grading assistant, we would have to train it on the type of assignments that would be turned in and a reasonable range of correct answers.

There are many different types of assignments that can be assigned to students. Some professors require hand written assignments. This would be difficult to implement since pen and paper is extremely unstructured and unorganized. Different students write in different styles and may organize their papers differently. Unless each student was precise on clearly labeling the question number and the answer, it would require a lot of data to properly analyze the format. This is ignoring other issues like accurately detecting messy handwriting. For the complexity and data required, we are not going to support handwriting.

If we have people submit word documents, there could also be some issues with how people format the questions and answers. We would run into a similar problem with handwritten assignments. It is theoretically possible, but it would require a lot of training data and more configuration to handle each assignment. We can save this challenge for a future project.

However, if we narrow down our field to work with free response questions online, we might have better success. This is because the expected input is well structured. There is a given question and a given answer. This would reduce the number of potential issues with question-and-answer detection to almost 0.

The last issue would be to determine whether a given answer is correct. This can be quite tricky as some questions may need to be in the ballpark of a right answer, while others need to include certain details. Ultimately, if we include certain sets of keywords that specify a given topic, we can detect if one of those keywords is in the answer. Using those flags, we can combine it with example data to train a model on what is a good answer.

# Skills Developed

I think it is safe to say that I learned a lot of different skills in these two classes alone.

When it comes to text analysis, I think my experience with the chatbot software Rasa was very important. Rasa showed me how a group of words or phrases can be grouped together to indicate a particular field or to have different intents. If we used this same concept with our grading program, we could easily ensure that different fields are met for various answers. If a piece of needed information is missing, we can detect that and include it in our feedback. If there are different terms for the same concept, we can detect and ensure that information is included. It was also quite helpful to see how different

Another great tool that I learned is Automation Anywhere and UiPath. These are both great RPA tools to help make automation easier. With a little bit of configuration, we can specify a set of tasks to complete to make inputting and outputting data much faster and easier. Earlier in this experience, I was able to use both of these tools to automatically process applications to make the data easier to view. This is a relatively simple task for a human to do, but it takes a lot of precious time. With hundreds of applications, it can become very overwhelming and error prone. A few simple instructions and configuration were able to process each application into a format that was easier to process for future needs. These are very complex tools that have a lot of potential for future automation projects.

# Theoretical vs Practical Knowledge

A lot of the theoretical knowledge that I have comes from our discussions of ethics and the potential consequences if we misuse these types of tools. I know that AI has the potential to be wrong. It is not infallible and is unpredictable by nature. We can train it as best as we can with a diverse dataset, but that is not a guarantee that it will behave as we would expect it to. We should **expect** it to fail and to gracefully handle scenarios when it does not work as we intended.

This is why I strive to design human-centered AI tools. AI is not a replacement for human work. Just because we could replace some jobs with AI does not mean that we should. It is a tool to help complete tasks that would be too difficult or tedious for humans to do alone. However, any important decision that could affect one’s life or business should always be reviewed by a human to ensure that there are no unforeseen consequences.

On the practical side of things, there are a lot of disparities between the ethical knowledge and considerations compared to the reality of how we make ethical AI. It is easy to say that we will try to reduce bias and incorporate safeguards to ensure that everyone is treated fairly. However, actually making that system is hard. There are a lot of ways in which a system can accidentally be trained to produce biased output. There are ways in which we can mitigate that risk, but it requires a lot of time and data.

There is also a big difference between saying we will train AI to complete this task with actually training it to complete said task. AI requires data and as a student, it can be hard to collect data for a specific problem. Generating my own data can be difficult and has the potential to negatively influence how the system will train. My own data would follow a certain pattern to it that other students may not replicate.

There are a lot of differences between the theoretical and practical side of building automation tools like this. Ethics and safety need to be a top priority while also finding ways to ethically source the needed data.

# Personal Reflection

As I’ve previously stated, using AI ethically is my number one priority. I want to ensure that these powerful tools can not be used to accidentally or intentionally harm, discriminate, or misinform anyone. This may come at the cost of speed and progress of development, but I truly believe that the risks far outweigh the rewards.

If I work on this type of technology in a professional workplace, I will be one of the first people to pause and ensure that we are taking everything into consideration before moving forward. We need to think about the positive and negative impacts it may have on others. We need to think and mitigate possible sources of bias or misinformation. We need to consult others for their opinions as our own experiences limit what we are knowledgeable on. Our design philosophy should be human-centered rather than human-replacement. Once we are reasonably certain that any possible negative impact is mitigated, we can begin working on the project.

This may seem a bit unreasonable to people that are focused on progress and profits, but it is necessary to ensure the safety of everyone. We have the potential to create an immensely powerful tool and should treat it responsibly. We need to ask if we should before we ask if we could.

On the more technical lessons learned, I believe that I am more than ready to develop useful tools that can change how we work and process data. I work in a few volunteer organizations that has to handle budgeting paperwork and shopping lists. This work can be quite tedious and wasteful since it is done by a volunteer. I can see a future in which this work is adapted to incorporate RPA tools to help automate these tasks quickly so people can focus on what matters most in an organization.

# Personal Opinion

These classes gave me a more unique insight on Cognitive Automation and Robotic Process Automation. Tools I never thought were possible are being developed and used today. It is kind of incredible to think about the current time that we are living in.

With all of our weekly discussions and numerous essays written, I've come up with a few key points for myself when it comes to AI:

1) AI must be used responsibly and ethically. Bias, misinformation, and impact need to be considered.
2) These tools are not replacements for people and their jobs.
3) AI is not a magic wand. It is a tool and should be viewed as such. It can help with problems, but it can not be trusted to solve every problem by itself.
4) AI should be human-centered in design.

I think that the future is bright in this space if and only if we use this technology responsible. I may be hesitant to embrace new technologies at times, but I am excited to see what good we can do for everyone.
