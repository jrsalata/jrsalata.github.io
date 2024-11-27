---
title: "My GitHub Copilot Experience"
date: 2024-11-27T08:24:09-05:00
description: "Hear my thoughts and experiences with these new AI tools that bring unease to some"
author: "John S"
draft: false
toc: true
---
# It's Just A Rock
With the rise in complexity and power of generative AI tools, there are a few important details that I like to keep in mind.
0. It's just a rock. The very first lecture I attended started off with this simple lesson and reminder from [Andy Harris](https://librarything.com/author/harrisandy-1). Computers aren't magic. They have a set way of doing exactly what you tell them to do. Any behavior is a result of either the developer or the user telling the rock to do something. The same idea applies with AI.
1. Artificial Intelligence is just spicy math. AI does not 'know' anything the same way humans do. We have an understanding of the world around us and how everything interacts with one another. AI has a _guess_ as to how different pieces of data connect with each other. It is nothing more than a mathematical black box. We don't entirely know how it processes data and how it comes to the conclusions that it does. Is it impressive? Absolutely. Is it this all-knowing power that some treat it like it is? No. Not even close.
2. Artificial Intelligence is a **tool**, not a human replacement. We've seen individuals use AI to create essays, write code, and handle basic troubleshooting. However, it is not a replacement for individuals who are great writers, coders, and technicians. Once again, AI doesn't truly understand what it is talking about. It just has an idea. As of now, a skilled human will be more reliable than an AI at creating a desired product. However, that is not to say that skilled individuals can't benefit from AI. AI can make it easier to get feedback, ask questions, and handle repetitive tasks. 
3. Artificial Intelligence has a lot of ethical and legal considerations around it. After all, it requires massive amounts of data to train and develop. Most of that data comes from the internet where many did not give explicit consent for their data to be used to train these models. There are many nuances to the legality and morality of using AI tools, especially for artwork. However, this is a full topic for another day. For now, let's just say that it is important to review your use of AI and ensure that it is ethical and human-centered.

# GitHub Copilot
With these points in mind, let's focus in on a tool I have many opinions about: [GitHub's Copilot](https://github.com/features/copilot). This past semester, I gained access to GitHub Copilot thanks to [GitHub Education](https://education.github.com/learner/learn), which provides special access to various tools and services for being a verified student. To any students reading this, I **highly** recommend checking it out for your personal account. But I digress.

To start out with, let's look at how GitHub advertises Copilot. On their main page, they describe it as "Your AI Pair Programmer" and I think that is the most accurate way to describe this tool. After all, that is what AI is. It is a tool, not a replacement. 

# First-Year Students Effect
In my experience as a TA for our intro level CS course, I saw a lot of people use Chat-GPT or [Replit's AI](https://replit.com/ai) to solve problems for them. Many of them struggled when their code wasn't working because they didn't learn _why_ the code worked. Just that the magical AI box generated it and that it _should_ work. The same goes for blindly copying and pasting snippets from Stack Overflow without stopping and asking why it works.

My philosophy when it comes to learning a new skill is to ask why something works and not just what or how. I would always redirect students to asking the critical question of why we are doing something. Frequently, they would struggle to explain their thought process with how they developed the code on the screen because they didn't develop it. At this point, I would hand them a whiteboard marker and we would go through the problem and develop an algorithm for it. Once we developed an algorithm, we would work together on the code and understanding _why_ we wrote specific lines.

This anecdotal evidence shows that these tools are not replacements for actual work. In fact, they can be a blocker to learning how to code or use a new language. So if these tools are not replacements, what are they good for?

# My Experience
## Autocomplete
I cautiously enabled Copilot on my machine to see how well it works and I have a few thoughts. First of all, the automatic code generation tends to get in my own way. Before starting a section, I need to first decide on the problem I'm trying to solve, how I'm going to solve it, and what I need to keep in mind while solving it. Copilot provides suggestions while coding and it requires me to stop what I am doing for a second, consider this snippet in front of me, decide if it is what I want to do, and either accept it or try to get back on track with my train of thought. It is like having a person breathing down your neck and telling you what to do before you can think. Even with good comments, it tends to produce janky code that misunderstands the greater vision with the project. This makes sense. It is a tool that is great for small sections and not completing the entire project with a few prompts. I ended up disabling the completions all together since it was too distracting. 

The one situation that made reenabling autocomplete worth it was when writting constructors, getters, and setters for an object. By simply defining the different variables, it was able to generate each barebones method with ease. This code was no different than the one I was going to write anyways, so I see no problem with using it. By handling the boilerplate under my supervision, I was able to save myself a few minutes of tedious typing. 

## Chat and Error Explaination
Where Copilot really shines is in its explanation and chat features. It is able to look at error logs and explain what a particular error means and how to potentially fix it. This was really beneficial when I ran into a few issues that I couldn't figure out. Copilot was able to explain it to me in a way that made sense and my solution for fixing it matched with what it recommended. By making error information and documentation easy to access, it makes it a lot faster to know what to type if you understand exactly what it is you are trying to do. 

Now, keep in mind that I always made sure to understand why it was going to do something before I let it do its thing. If I do not understand a problem, then I need to learn and ensure that the solution makes sense. While uncommon, there were times that it was wrong and gave me code that would have made the issue worse. 

The chat window is also useful for asking it questions on different methods and options for a task. For example, I needed a way to store a HashMap in Java but needed to keep a list of the elements in order of their insertion. I consulted Copilot and it directed me to the documentation for a LinkedHashMap, which kept the elements in their insertion order. This fast consulting tool made it easy to do research and learn about data types I didn't know existed. I was able to verify the information and look into it a bit more because of the starting point Copilot gave me.

# Conclusion
GitHub Copilot is a good tool if you know what you are doing and looking for a tool that can help when switching between languages, asking questions, or analyzing errors. It works best when you, the programmer, know what is going on and what needs to be done. It is not a replacement for programmers or a way to give students solutions to problems. It is an enhancement on an already defined skillset. 

I see a lot of potential for future AI tools in the field of software development, but I am far from convinced that it is going to take over our jobs simply because it still requires a decent amount of expertise to understand it.