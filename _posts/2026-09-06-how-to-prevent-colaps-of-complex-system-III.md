---
layout: post
title: "How to prevent colaps of complex system"
subtitle: "Part III - practical. What to do and some hints"
date: 2026-09-06 08:00:00 +0300
background: '/img/sea-creatures/sea_creatures17_wall.jpg'
---

Previously I described [How to prevent colaps of complex system - Part I](/2025/02/16/how-to-prevent-colaps-of-complex-system-I.html) and [Part II - practical. Is it possible to predict the fail](https://octadero.com/2025/02/17/how-to-prevent-colaps-of-complex-system-II.html)

### What Makes Difficult and Complex Systems Stop?

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


### Preventing irreversible movements  
While predicting an irreversible event may not be possible, it is your responsibility to evaluate the stability of your system. One approach is to create a simple numerical model that tracks the system's entropy levels. This can help you understand when the system is heading toward instability.  

### Types of complexity and how they differ from difficult systems  
Minimizing complexity is relatively straightforward. The first step is to understand the types of complexity present in your system. You might be surprised to find that your system contains different kinds of complexity. Here are two key types:  

- **Essential Complexity:** This includes factors like domain complexity, scale, parallelism, uncertainty, ambiguity, interdependencies, and dynamic behavior. Some level of complexity is inherent and necessary for solving real-world problems. Our world is interconnected, and our systems must reflect that complexity to interact effectively with the environment.  

- **Accidental Complexity:** This type arises from poor design decisions, suboptimal practices, technical debt, overengineering, inconsistent tooling, configuration issues, and organizational constraints. For example, a system might become unnecessarily complex due to a lack of quality architecture or using a variety of technologies without proper integration. 
Consider a scenario where different third-party services are used for push notifications across platforms (iOS, Android, Web), each with a unique API and workflow. Similarly, mixing old legacy systems (e.g., MySQL for statistics) with newer systems (e.g., PostgreSQL for BI) can add complexity. The complexity of maintaining multiple operating systems on a GPU computation cluster (e.g., CentOS, Ubuntu, Red Hat) or managing different versions of Python or CUDA can become overwhelming.  

### Basins of Attraction

Any dynamic system has two important characteristics: **inertia** and, less commonly discussed, **basins of attraction**.

Both concepts describe how a system behaves dynamically. Inertia is well understood: it represents the system’s resistance to changes in its current state. Basins of attraction are more complex and, in my opinion, particularly useful for understanding how real-world systems evolve.

A **basin of attraction** describes the tendency of a dynamic system to converge toward a particular value, configuration, or state. While inertia can be thought of as resistance to movement, a basin of attraction describes **where the system tends to move and how difficult it is to move it somewhere else**.

You can imagine the system as a ball moving through a landscape of hills and valleys. The ball will naturally roll toward one of the valleys. Once it is there, it may be relatively stable, and moving it into another valley requires additional energy. The deeper the valley, the harder it is to escape.

This concept can also be applied to technology and organizations.

For example, consider a legacy technology solution. It may be difficult to change or replace, but it provides a certain level of stability and predictability. Over time, the organization effectively settles into its "basin of attraction": changing direction becomes increasingly expensive, even if the alternative is technically better.

Another example is choosing a cloud-based data-labeling provider. The provider may automatically import all your existing data and even offer technical assistance with the migration. This makes moving into the platform extremely easy. However, once your data, workflows, and processes depend on its proprietary formats and APIs, moving out can become significantly more difficult.

The same applies to organizational decisions. Imagine a decision to reduce part of a team. Executing the decision may be relatively easy, but reversing it later can be much more expensive—in terms of both money and time. Once people leave, rebuilding the same expertise and team structure is not simply a matter of reversing the original action.

This leads to an important consequence: **when making a decision, we should consider not only the resources required to move the system into a new state, but also the cost of moving out of that state later.**

In other words, the real cost of a decision is not always the cost of reaching the next state. It also includes the **shape of the basin we are moving into**—how stable it is, how difficult it will be to escape, and what options it leaves us for the next step.
