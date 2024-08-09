---
layout: post
title: "The decline of von Neumann's architecture"
subtitle: ""
date: 2024-08-09 10:15:00 +0300
background: '/img/posts/introduction@2x.jpg'
---
 For more than 30 years computers have been so popular and common that we can't imagine our life without them. They have become more than a tool to calculate your home taxes and a communication device that pushes out paper letters. We always tend for a new way to extend our reality and we want to develop new machines with new skills. As the computation level increases, it becomes more difficult to make a new step. Today we faced with long list of limitations:


## The Decline of the von Neumann Architecture You've Never Heard of and What’s Next?

Over the past thirty years, computers have become so popular that they have transformed many processes in human life and society. Each year, according to Moore's Law, they gain more computing power, enabling them to solve increasingly complex tasks. Today, however, computers face several limitations that prevent us from tackling the challenges depicted in futuristic movies. Will this continue, is there a limit to modern architecture, and what should we do if this rapid growth is no longer possible?

#### Disclaimer

The von Neumann computer will continue to handle tasks related to relational databases (though I'm not sure about Big Data), numerical methods, the internet, etc. It will still do everything it was designed to do, but we won't see the same rapid increase in computing power. For solving real-world signal processing tasks, a different architectural approach will be used. Both architectural approaches will be employed on a single printed circuit board, and eventually, in a single chip.

# The Classical von Neumann Architecture

## The “Bottleneck” of the von Neumann Architecture

All classical computers have the so-called von Neumann architecture. The disadvantage of this architecture is that data from the memory area must be transferred to the computational unit area and back, cycle by cycle. The interface linking the computational unit and the computer memory is limited in bandwidth. Even the fact that modern processors have several levels of cache directly within the computational unit does not solve the problem. This approach is exacerbated by the need to accumulate and structure data to fully fill the buffer of computed operations. A metaphor can be used: the train won’t move until all passengers have taken their specific seats.

## Physical Limitations of Materials

According to Moore's Law, the number of transistors doubles approximately every two years while reducing production costs. This is achieved by reducing transistor size. However, this reduction leads to another limitation: the size is determined by the physical properties of the materials used to make them. The reality is that this law is starting to face pressure from the "laws of micro-world physics."

## Resilience and Manufacturing Defects

Have you ever wondered how lower-end models of processors and graphics card chips are made? You might think that dedicated teams design a new simplified chip every year. In reality, the process looks different. A company develops one maximum-power chip with a repeating architecture. Almost all elements are duplicated, just like in aviation. This is done so that if a significant number of processors in one block fail due to manufacturing defects, the block can be disabled while the processor as a whole remains functional. As you might imagine, processor production is very expensive, and one reason for this is the high defect rate. For instance, the defect rate for 28-core Intel Xeon processors can reach up to 65%. If a final processor has a defective memory block or one core fails the TDP test, it is disabled, and the processor is packed as a "junior model."

## Power Consumption and Size of Supercomputers

In the modern world, where a mobile phone has the computing power of a five-year-old computer and runs on a battery, it seems we have nearly reached the limit in reducing computer power consumption. However, if we compare the computing power, size, and energy consumption of the IBM Summit supercomputer with a mouse's brain, we find that the supercomputer is enormous and highly inefficient. The IBM Power System AC922 has 2.41 million cores and consumes 13,000,000,000 W, occupying a space of 920 m³. In contrast, a mouse's brain, which can handle far more complex tasks, consumes only 1-5 watts.

## Online Learning and Continuous Flow

Here, I would like to talk more about algorithms than architecture, although, in this context, algorithms are dictated by architecture. The modern computer handles discrete data well, even when there is a large quantity of it. However, when it comes to sequences, continuity, or infinitely small or large values, we try to find some approximation. Consequently, we interpret our data into a sequence of discrete frames, breaking, dividing, and processing each frame as something static and finite. Yes, various approaches exist, such as bi-directional soft attention (see BERT) to connect these frames in language models. However, modern machine learning approaches still lack the ability to learn directly in the process of solving a given task. These are still two different tasks.

## Parallelism and Scalability

Returning to the von Neumann architecture, we see that all data flow passes through a central computational center, creating yet another bottleneck. The number of cores in modern chips is increasing, but this introduces a new problem: first, data must be parallelized, and then results synchronized. So, if you have many independent input signals, unrelated in time or context, multiple processor and graphics card cores handle this task well. However, if you have a large input signal, the task of parallelizing computations and synchronizing results can occupy most of the computation time.


## Neuromorphic Inspired Computing

As early as 1950, Turing and von Neumann described architectures resembling our brain, but unfortunately, at that time, neither neurophysiologists had a clear understanding of how the brain worked, nor did physicists know what the physical components of such a computer might look like. This does not mean that neurophysiologists now have all the answers about the brain’s structure or that physicists can propose a perfect physical foundation for such computers, but I believe we can already begin developing the first of these computers.

To start a discussion on neuromorphic architecture, we should begin with the neuron. There is so much basic information about the structure of a neuron in various publications on machine learning that I will try to summarize it briefly and move directly to a very superficial description of its functionality. I will also frequently refer to an abstract "brain." This reference should be taken lightly, understanding that neurophysiologists know very little about its structure, and I am merely superficially relying on some of these notions.

Another important point to mention is that modern approaches in neuromorphic architecture do not attempt to create an exact "copy" of the brain in "silicon." Firstly, as I mentioned earlier, neurophysiologists know very little about how the brain actually works. Secondly, the physics of the process will differ, meaning some approaches cannot simply be transferred from one system to another. Thirdly, we have learned to solve certain tasks better and more efficiently than our brains. Finally, the brain solves many side, non-cognitive tasks, such as regulating body temperature, controlling hormonal glands, etc., which do not need to be reproduced at this time.

#### What interests us in the brain's structure?

The brain of a living organism is a combination of a large number of very small computational elements (neurons), which, in turn, are quite independent of each other. Each neuron stores and processes a minute amount of knowledge from the creature's overall memory. If individual neurons fail, neighboring neurons take over the tasks of the dead ones. Specific parts of the brain are well specialized. Neurons not involved in solving a specific task consume almost no energy. The human brain consists of 86 billion neurons, enabling us to process a vast amount of signals simultaneously.

An interesting fact is that neurophysiologists, not engineers, physicists, or mathematicians, played an active role in creating the new architecture. Neurophysiologists, in the process of studying the brain, built mathematical models of individual parts of the brain, which they then attempted to calculate on computers. As these models became more complex, they realized that calculating such models on existing hardware was inefficient, necessitating a radically new approach.

#### The Neuron

Discussing neuromorphic computers, we cannot avoid the topic of neuron structure. Any article on classical machine learning and neural networks provides an idea of how a neuron is structured and how it functions. I will not repeat the basic works of neurophysiologists.

For now, we don't need to study the structure of the neuron in detail to understand its basic functionality. We are only interested in its four main parts: dendrite, nucleus, axon, and synapse. I will list the elements whose working principles are important for solving our tasks.

It is worth noting that neurons come in various types and kinds, each characterized by different functionalities. There are also numerous types of synaptic connections. But we will only need this when we move on to topologies. For now, it is important to remember that a neuron is much more complex and diverse than, for example, ordinary transistors.

Like a transistor, a neuron acts as a kind of gate in the path of a signal, but the decision to transmit the signal and its final form (the signal) is determined by more complex mechanisms than a transistor. When talking about a neuron, one can speak of several levels of these mechanisms, where each of them plays an assigned role.

To summarize, the neuron receives input signals through many dendrites, and if the total signal exceeds a certain threshold, the neuron generates its signal and sends it to the next neuron using its axons.

---

[1] J. Von Neumann and R. Kurzweil, The computer and the brain. Yale University Press, 2012.

[2] A. M. Turing, “Computing machinery and intelligence,” Mind, vol. 59, no. 236, pp. 433–460, 1950.

[3] nanoCMOS Device, Circuit and System Simulations, https://cnx.org/contents/hMLR8R0g@1/nanoCMOS-Device-Circuit-and-System-Simulations

[4] Types of neurons, https://qbi.uq.edu.au/brain/brain-anatomy/types-neurons

[5] Computing complex visual features with retinal spike times Gütig R, Gollisch T, Sompolinsky H, Meister M (2013)

[6] Industrial DVS Design; Key Features and Applications http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Eric_Ryu_Samsung.pdf

[7] Spike-shape dependence of the spike-timing dependent synaptic plasticity in ferroelectric-tunnel-junction synapses, https://www.nature.com/articles/s41598-019-54215-w/

[8] Benchmarking Keyword Spotting Efficiency on Neuromorphic Hardware, https://arxiv.org/abs/1812.01739

[9] Advancing neuromorphic computing From promise to Competitive technology, https://niceworkshop.org/wp-content/uploads/2019/04/NICE-2019-DAY-2a-Mike-Davies.pdf
