---
layout: post
title: "How to prevent colaps of complex system"
subtitle: "Part II - practical. Is it possible to predict the fail"
date: 2025-02-18 21:08:00 +0200
background: '/img/sea-creatures/sea_creatures17_wall.jpg'
---

[How to prevent colaps of complex system - Part I](/2025/02/16/how-to-prevent-colaps-of-complex-system-I.html)
Previously I described systems

### Size, mirage of regularity, Lack of understanding and control
First call 

## Preventing irreversible movements  
While predicting an irreversible event may not be possible, it is your responsibility to evaluate the stability of your system. One approach is to create a simple numerical model that tracks the system's entropy levels. This can help you understand when the system is heading toward instability.  

### Types of complexity and how they differ from difficult systems  
Minimizing complexity is relatively straightforward. The first step is to understand the types of complexity present in your system. You might be surprised to find that your system contains different kinds of complexity. Here are two key types:  

- **Essential Complexity:** This includes factors like domain complexity, scale, parallelism, uncertainty, ambiguity, interdependencies, and dynamic behavior. Some level of complexity is inherent and necessary for solving real-world problems. Our world is interconnected, and our systems must reflect that complexity to interact effectively with the environment.  

- **Accidental Complexity:** This type arises from poor design decisions, suboptimal practices, technical debt, overengineering, inconsistent tooling, configuration issues, and organizational constraints. For example, a system might become unnecessarily complex due to a lack of quality architecture or using a variety of technologies without proper integration. 
Consider a scenario where different third-party services are used for push notifications across platforms (iOS, Android, Web), each with a unique API and workflow. Similarly, mixing old legacy systems (e.g., MySQL for statistics) with newer systems (e.g., PostgreSQL for BI) can add complexity. The complexity of maintaining multiple operating systems on a GPU computation cluster (e.g., CentOS, Ubuntu, Red Hat) or managing different versions of Python or CUDA can become overwhelming.  

### The Budget of Complexity  
The **budget of complexity** refers to the limited resources (money, engineers, time) available to manage complexity in a system. It's important to remember that these resources are finite, so managing complexity efficiently is crucial.  

One of your main tasks should be minimizing **Accidental Complexity**. If a service, tool, or class has multiple implementations that aren't required by your specifications or aren't serving a critical purpose (e.g. reservation), you should unify them. 
====>
Minimising **third-party relationships** by creating self hosted solutions is not the best practice from my point of view. You product I suppose has main one feature where you and your team is expert of. Deploying self-hosted solution is reasonable only if you have clear understanding how to will do better then team for whom that service their main feature. Better then service who has years of experience growning it. Better strategy will be defining what that provider can and can't to do. How many notifications it can deliver, how often maintaining window it has and for how long, what SLA it can serve. Think about monitoring third party services and have backup strategy. Maybe you need to replace it by some bore relaiable and maybe more expensive.

Respect your legacy code. If it is simple to understand, stable, and rarely updateble code - leave it as is. It can use old patterns, it can be outdated from of view modern concepts. If your data flow and processing pipelines has some primitive OpenCV preprocessor with lot's of simple instructions, you should not replace it by some cloud based modern third paty mouse configurable service. I can assume there are thesame OpenCV code under the hood.

You need to answer on questions:
What part of your system you can't describe in numbers (how much requests you can handle, how time does it take to make change in the code, etc). Start tracking you system in numbers charactarising different aspects of it.


# Positiva & Negative feedback  => stock market, key feature, one customer => diversification

# Basins of attraction

# So big complex system
How easy your system to adopt it or make changes?
Flaxibility & scalability