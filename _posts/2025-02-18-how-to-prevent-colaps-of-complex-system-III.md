---
layout: post
title: "How to prevent colaps of complex system"
subtitle: "Part III - practical. What to do and some hints"
date: 2026-10-18 08:43:00 +0200
background: '/img/sea-creatures/sea_creatures17_wall.jpg'
---

[How to prevent colaps of complex system - Part I](/2025/02/16/how-to-prevent-colaps-of-complex-system-I.html)
Previously I described systems

## What Makes Difficult and Complex Systems Stop?

As you may remember, **difficult systems are generally linear**, while **complex systems have nonlinear relationships and interactions between their components**.

This difference leads to fundamentally different behavior when something goes wrong.

In a **difficult system**, a failure of a single component can cause the entire system to stop, especially if the system was designed with a fail-safe or backup mechanism. The system may stop immediately, but the failure is usually **predictable and relatively easy to diagnose**. It is often possible to identify the failed component and determine the root cause quickly.

In a **complex system**, failure analysis can take hours, days, or even months. Some complex systems can compensate for a broken component by replacing its functionality with another mechanism or an artificial workaround. As a result, the system may continue operating, and the original problem can remain hidden behind what appears to be normal behavior.

This is what makes complex systems particularly difficult to diagnose. When the system eventually stops, you may initially spend significant time investigating and fixing **symptoms or secondary effects rather than the actual root cause**. You may even end up debugging a workaround that had previously masked the original failure.

Therefore, in complex systems, the most difficult part is often not fixing the failure itself, but **understanding what actually failed in the first place**.


### Size, mirage of regularity, Lack of understanding and control
A complex system can be small if you measure it by the number of components, the size of its inputs and outputs, or its overall scale.

However, **size does not make a system complex**. Complexity comes from the **type, number, and interactions of relationships between its components**.

A complex system can be a team of just four engineers, a service with only a few features, or a company with ten employees.

For example, a small team can develop highly complex relationships and responsibilities. When there are no departments, clearly defined processes, strict roles, or well-established responsibilities, one person may have to handle many different areas. It may also be unclear where one person's responsibility ends and where another person's responsibility begins.

In such an environment, much of the system depends on **historical agreements, implicit knowledge, dependencies, and personal relationships** rather than clearly defined processes.

This means that the smaller the organization or system is, the **higher the chance that it behaves as a complex system rather than a difficult one**.

The key distinction is not how big the system is, but **how its parts interact and how predictable those interactions are**.

When you look at a **large, difficult system**, there is a good chance that you can see most of its real size. Its components, structure, interfaces, roles, and dependencies are usually visible and can be mapped.

When you face a **small, complex system**, be prepared for the opposite: **you may not be able to see its real size**.

The visible system may consist of only a few components, people, or features, while the actual complexity is hidden in the relationships between them. These relationships may be based on history, implicit agreements, personal knowledge, and dependencies that are not documented anywhere.

The system may look small from the outside, but its **invisible network of relationships can be enormous**.

As Antoine de Saint-Exupéry wrote in *The Little Prince*:

> “It is only with the heart that one can see rightly; what is essential is invisible to the eye.”

The same principle applies to complex systems: **what makes them complex is often not what you can see, but what exists between the visible parts.**


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
