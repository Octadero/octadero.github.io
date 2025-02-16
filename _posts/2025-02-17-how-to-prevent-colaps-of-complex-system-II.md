---
layout: post
title: "How to prevent colaps of complex system"
subtitle: "Part II - practical. Is it possible to predict the fail"
date: 2025-02-17 21:08:00 +0200
background: '/img/sea-creatures/sea_creatures17_wall.jpg'
---

Previously, in [Part I](/2025/02/16/how-to-prevent-colaps-of-complex-system-I.html), I discussed the differences between difficult and complex systems. In this article, I'll focus on the practical markers that often precede the collapse of a system.  

![Complexity Illustration](https://octadero.com/img/posts/2025-01/attractors-dequan_0.jpg)

### Size, Mirage of regularity, Lack of understanding and control  
The first and most straightforward factor is the **size** of your system. Everything is relative, and by size, I mean the proportion of the system's complexity to the team responsible for maintaining it. From my experience, an engineer typically begins to lose familiarity with a section of code about 3-6 months after they last worked on it. This makes it crucial to decompose your project into manageable features and regularly review how often team members revisit older parts of the codebase. Tools like **Codescene** can help track code familiarity and identify areas of concern.  
It's also essential to define clear ownership for each part of the product, analyze overlaps, and identify features without a dedicated maintainer.  

Another potential pitfall is the **mirage of regularity**—the illusion that a complex system is more predictable or orderly than it truly is. A key indicator of this is your team's ability to estimate timelines for changes or new features. If you notice a growing discrepancy between your predictions and actual deadlines, it's a sign that complexity is increasing.  

Consider a scenario where no one on your team can confidently answer questions like "How do we adapt this feature?" or "How can we change this functionality?"—even after days of reviewing the codebase. Worse still, if the proposed solution becomes "It's easier to rewrite this from scratch," and the entire team agrees, then you're facing a **lack of understanding and control** over your system. This is a clear warning sign of rising complexity.  


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

Minimizing **third-party relationships** by developing self-hosted solutions isn't always the best approach. Your product likely has one core feature where you and your team excel. Deploying a self-hosted solution is only reasonable if you have a clear understanding of how you can outperform the team whose primary focus is that service—one that has spent years refining and scaling it.  

A more effective strategy is to clearly define what the third-party provider can and cannot do. Understand their limitations, such as the maximum number of notifications they can deliver, the frequency and duration of maintenance windows, and their SLA commitments. It's also wise to monitor third-party services and have a backup plan in case of failures. In some cases, switching to a more reliable (and possibly more expensive) provider may be necessary.  

Respect your legacy code. If it's easy to understand, stable, and rarely needs updates, it's often better to leave it as is—even if it uses outdated patterns. For example, if your data processing pipelines use a basic OpenCV preprocessor with simple instructions, there's no need to replace it with a modern, cloud-based, third-party service. Chances are, the new service is just repackaging the same OpenCV functionality under the hood.  

Ask yourself these questions:  
- Which parts of your system can't you quantify (e.g., how many requests can it handle, how long does it take to implement a change)?  
- Are you tracking key metrics that characterize different aspects of your system's performance?  

By understanding your system in measurable terms, you can better manage complexity and make informed decisions.

Next and final part will include **Positiva & negative feedback loop**, **Basins of attraction** and some conclusions.