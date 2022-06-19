---
layout: post
title: "The decline of von Neumann's architecture"
subtitle: ""
date: 2022-06-19 10:15:00 +0300
background: '/img/posts/introduction@2x.jpg'
---
 For more than 30 years computers have been so popular and common that we can't imagine our life without them. They have become more than a tool to calculate your home taxes and a communication device that pushes out paper letters. We always tend for a new way to extend our reality and we want to develop new machines with new skills. As the computation level increases, it becomes more difficult to make a new step. Today we faced with long list of limitations:

Von Neumann Bottleneck:
[IMAGE]
The classic computers has the same architecture:
 Processor, Memory and Data bus between them. Information is always moving from memory to processor and back to memory. It looks like a road from downtown to the center of the city in the morning, as much data and instructions we need to process by CPU as much this road must to be.

Device and materials limits:
[IMAGE Origin of atomic scale variability in nano CMOS transistors]
The process of making transistors smaller and smaller tends to cause more and more faults in devices. That leads to a higher cost of one device unit and a huge waste of materials, time, power and so on. Any new generation of processors doesn't cost us less money. 
>[3]Until recently the transistors in silicon chips were assumed to be of uniform design, having identical physical properties and characteristics. However as illustrated in Figure 1, as transistor dimensions approach the nanometer scale this assumption no longer holds true with microscopic differences in atomic structure, doping configuration and material granularity producing differences in the macroscopic behavior of individual devices.
As a result, Moore’s Law is now reaching the physical, atomistic limits of silicon and radical new approaches are needed that encompass this atomistic variability.

Power consumption, Size :
[IMAGE - IBM Summit]
Let's look on supercomputer IBM summit: IBM Power System AC922, IBM POWER9 22C 3.07GHz, NVIDIA Volta GV100, Dual-rail Mellanox EDR InfiniBand, 2.41 million cores, 148.6 petaflops
Peak Power Consumption: 13 000 000 000 W
Size: 4,608 nodes  * 0.2 m^3 = 920 m^3
That means that the most expensive device which cost half a billion dollars is taking football court and consume a lot of energy and at the same time it can't 

The idea of using custom hardware to implement neurally inspired systems is as old as computer science and computer engineering itself, with both von Neumann [1] and Turing [2] discussing brain-inspired machines in the 1950’s. Computer scientists have long wanted to replicate biological neural systems in computers. This pursuit has led to key discoveries in the fields of artificial neural networks (ANNs), artificial intelligence, and machine learning. The focus of this work, however, is not directly on ANNs or neuroscience itself, but on the development of non-von Neumann hardware for simulating ANNs or biological neural systems. 
 
Real-Time Performance
Parallelism
Scalability
Lower Power consumption - The most popular motivation in present-day literature and discussions of neuromorphic systems in the referenced articles is the emphasis on their potential for extremely low power operation. Our major source of inspiration, the human brain, requires about 20 watts of power and performs extremely complex computations and tasks on that small power budget. The desire to create neuromorphic systems that consume similarly low power has been a driving force for neuromorphic computing from its conception [18], [19], but it became a prominent motivation about a decade into the field’s history

Footprint - Similarly, creating devices capable of neural network-style computations with a small footprint (in terms of device size) also became a major motivation in this decade of neuromorphic research. Both of these motivations correspond with the rise of the use of embedded systems and microprocessors, which may require a small footprint and, depending on the application, very low power consumption.
Fault Tolerance
Faster
Online Learning

Tiny Spikes: Two layers within a neural network contain groups of “neurons” with similar functions, indicated by color [blue, yellow, orange, and pink] in the illustration on the left. In the graphic on the right, those neurons are mapped to spiking neurons in an IBM TrueNorth chip. The spiking neurons are connected by gridlike “synapses” to other neurons in the same core, and to a row of inputs. Those inputs can generate spikes, which are then processed by the neural network.

[1] J. Von Neumann and R. Kurzweil, The computer and the brain. Yale University Press, 2012.
[2] A. M. Turing, “Computing machinery and intelligence,” Mind, vol. 59, no. 236, pp. 433–460, 1950. 
[3] nanoCMOS Device, Circuit and System Simulations, https://cnx.org/contents/hMLR8R0g@1/nanoCMOS-Device-Circuit-and-System-Simulations

[1] J. Von Neumann and R. Kurzweil, The computer and the brain. Yale University Press, 2012.
[2] A. M. Turing, “Computing machinery and intelligence,” Mind, vol. 59, no. 236, pp. 433–460, 1950. 
[3] Types of neurons
https://qbi.uq.edu.au/brain/brain-anatomy/types-neurons
[4] Computing complex visual features with retinal spike times Gütig R, Gollisch T, Sompolinsky H, Meister M (2013)
[5] Industrial DVS Design; Key Features and Applications http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Eric_Ryu_Samsung.pdf
[6] Spike-shape dependence of the spike-timing dependent synaptic plasticity in ferroelectric-tunnel-junction synapses
https://www.nature.com/articles/s41598-019-54215-w/
[7] Benchmarking Keyword Spotting Efficiency on Neuromorphic Hardware
 https://arxiv.org/abs/1812.01739
[8] Advancing neuromorphic computing From promise to Competitive technology. https://niceworkshop.org/wp-content/uploads/2019/04/NICE-2019-DAY-2a-Mike-Davies.pdf
