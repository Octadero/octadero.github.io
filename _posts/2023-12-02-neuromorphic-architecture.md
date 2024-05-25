---
layout: post
title: "Neuromorphic Architecture"
subtitle: ""
date: 2023-12-02 18:00:00 +0300
background: '/img/obstract_10.jpg'
---
### Earlyes
Already in 1950, Turing and von Neumann described an architecture resembling our brain, but unfortunately, at that time, neither neurophysiologists understood how the brain functions, nor did physicists know what the elemental basis for such a computer might look like. This doesn't mean that neurophysiologists now have all the answers about how the brain works or that physicists can propose a perfect elemental foundation. However, I believe that we can already start developing such computers.

The discussion about neuromorphic architecture should begin with the neuron. In various publications on machine learning, there's a wealth of basic information about neuron functionality. I'll try to summarize its structure and swiftly move to a very superficial description of its functionality. Additionally, I'll frequently reference an abstract "brain." Approach this reference with leniency, understanding that neurophysiologists know very little about its structure, and I'm merely superficially leaning on some of these concepts.

Another crucial point to note is that modern approaches in neuromorphic architecture don't aim to create an exact "replica" of the brain in "silicon." Firstly, as mentioned earlier, neurophysiologists have limited knowledge about how the brain truly operates. Secondly, the physics of the process varies, meaning some approaches can't be seamlessly transferred from one system to another. Thirdly, we've learned to solve some tasks better and more efficiently than our brain. Lastly, the brain handles numerous non-cognitive tasks like regulating body temperature or managing hormonal glands, for which there's currently no pressing need to reproduce these functions.

### What interests us in the brain's structure?

The brain of a living organism is a union of many very small computing elements (neurons), which are relatively independent of each other. Each neuron stores and processes a minute piece of information from the collective memory of the being. If individual neurons fail, neighboring neurons take over their tasks. Specific brain regions are well specialized, and non-participating neurons in a specific task almost don't consume energy. The human brain consists of 86 billion neurons, allowing us to process a vast number of signals simultaneously.

An intriguing fact is that neurophysiologists played a pivotal role in creating this new architecture, not engineers, physicists, or mathematicians. Neurophysiologists, while studying the brain, constructed mathematical models of its parts and attempted to compute them on computers. As these models grew in complexity, it became clear that computing such models on the existing hardware was inefficient, necessitating a radically new approach.

### Neuron

Discussing neuromorphic computers inevitably involves exploring the structure of the neuron. Any article on classical machine learning and neural networks provides an understanding of how a neuron is structured and operates. I won't reiterate the basic works of neurophysiologists.

For now, to grasp the fundamental functionality, we don't need an in-depth study of the neuron's structure. We're currently interested in just four of its primary parts: dendrites, nucleus, axon, and synapse. I'll list these elements, understanding the principles of their operation are crucial for solving our tasks.

It's worth noting that neurons come in various types and forms, each characterized by distinct functionality. There's also a wide array of different synaptic connections. However, we'll delve into these only when we move to topologies. For now, it's important to remember that a neuron is far more intricate and diverse than, say, conventional transistors.

Similar to a transistor, a neuron acts as a gate in the signal's pathway, but the decision regarding signal transmission and its final form is shaped by mechanisms far more intricate than those of a transistor. When discussing a neuron, it involves several levels of these mechanisms, each assigned a specific role.

As a reminder, a neuron receives input signals through numerous dendrites, and if the cumulative signal exceeds a certain threshold, the neuron generates its own signal and transmits it to the next neuron via its axons.

### Spike-Timing Dependent Plasticity

I'll skip details about `Long Term Potentiation` and `Long Term Depression`, potassium-sodium gates, synaptic gaps, neurotransmitters, and so on. I'll focus on a few key points:

Neurons, when combined, form highly intricate logical chains capable of processing complex signals. Some neurons conduct signals and act as integrators, while others act regressively, serving as a form of "brake" for the passing signal. When organized into complex topologies, a neural network can process and memorize complex signals.
The primary goal of a network of neurons (as I understand it) is to establish rules that enable the network to independently process the input signal. To adapt to an input signal, this mechanism of adaptation must exist at a physical level. Neural connections can change through the Spike-Time Dependent Plasticity mechanism [5]. Consequently, neurons can alter the shape of their cells, increasing or decreasing the shape or quantity of their dendrites, axons, and synapses. The initiation and control of such changes may stem from the fact that a neuron produced a spike approximately 20 ms before a subsequent neuron (from a topological viewpoint, things might be more intricate) in the network produced a similar impulse. Neurophysiologists have also observed the reverse phenomenon: if neuron A fired an impulse within <100 ms after neuron B, following it in the network, neuron A would diminish its "connectivity" with neuron B.

I want to draw your attention to the fact that in the life cycle of a neuron, it's not always the signal's amplitude or wavelength that matters but rather the time intervals between signals.

### Signal Sources

It's important to note that, much like the human brain, neuromorphic computers do not directly process discrete digitized signals. As mentioned earlier in the disclaimer, this architecture aims to process real-world signals:

- Sound processing and synthesis
- Human speech processing and synthesis
- Video stream processing and synthesis
- Processing various spatial sensors
- Decision-making tasks, for example, spatial orientation tasks
- Event-driven computation

Our eye, like the eyes of many other organisms, is structured in such a way that it's incapable of "seeing" and transmitting a complete image to the brain simultaneously. Photons of light hitting the optic nerve trigger changes in its state, after which the nerve then transmits a signal to the brain about the level of these changes. Similarly, neurons located in the eye filter out 90% of predictable information [4], such as homogeneously colored areas in the scene. It's more effective to transmit the contour of a certain plane and the color that fills it, especially if the object is in the peripheral vision. If peripheral vision detects something potentially interesting (like movement), the eye sends a signal to focus more attention on that point.

In neuromorphic architecture, sensors and preprocessed data are also used, reflecting changes in state rather than a complete representation of data. For instance, Dynamic Vision Sensor (DVS) cameras are employed, capable of transmitting a video stream equivalent to thousands of frames per second. Additionally, the sensitivity and power consumption of such cameras are an order of magnitude higher than standard ones [5]. A significant advantage of such cameras lies in their ability to work with each part of the scene separately.

Figure 1a and 1b were captured by a regular camera with different contrast settings. As seen, the images either show a general scene or a tram in a tunnel, but it's not possible to obtain this information simultaneously. The DVS camera (2) can provide the necessary contrast for each pixel in the frame.

The well-known MPEG video compression format is also based on the idea of generating changes between frames, followed by processing these changes rather than the entire frame.

Who and how solves the given task?

Neuromorphic architecture doesn't imply programming specific rules to solve a given task. Similar to other machine learning methods, neuromorphic architecture assumes that a programmer will create a structure (neuron topology) capable of self-learning. Once a certain result is achieved, their final state can be used as a ready-made solution.

It's worth noting that neuromorphic architecture resembles neural networks in classical machine learning tasks, but many mechanisms differ significantly. For this reason, knowledge about neural networks, on one hand, will help in understanding the discussed topic, but on the other hand, it can be quite perplexing.

### Software Implementation

The initial attempts to implement neuromorphic architecture were programs on IBM-compatible computers. Some projects, such as NEST, PyNN, Nengo, are still used for modeling specific brain regions. In comparative tests, simulator performance is lower [7]. However, comparing performance across different hardware approaches in synthetic tasks might be inaccurate. But comparing energy efficiency in solving the same task can be considered valid. In such tests, neuromorphic architecture demonstrates efficiency gains of 5 to 10 times [8]. Currently, these simulators are evolving into APIs for working with neuromorphic chips.

To begin working with neuromorphic architecture, there's no need to order boards or rent them in the cloud; one can explore this new approach using a simulator on a regular computer or server.

IBM TrueNorth, BrainScales, Intel Loihi

As of today, there are three major projects focusing on hardware solutions based on the idea of neurons. Each chip represents a matrix of interconnected neurons.

Let's consider the chip architecture using IBM TrueNorth as an example. It's built from a network of "primitive" neurosynaptic cores. The architecture implements connections of near-range cores with intra-core cross-memory directly and connections of far-range cores via inter-core spike transmission network. TrueNorth is fully programmable in terms of both the "physiology" and "anatomy" of the chip, meaning the programming of neuron parameters, synaptic grid (crossbar), and inter-core neuron-axon connections is possible.

The signal "passes" from axons to neurons controlled by binary synapses. Each axon is connected in parallel to all neurons in the core.

All synaptic connections are indexed, allowing access by their address. The network's operation is regulated by a discrete time step. Each cycle computes the state of the synapse: if the synapse value for a specific axon-neuron pair is non-zero and the axon is active, the neuron updates its state using the synaptic weight corresponding to the axon type. Then, each neuron produces resulting activity. A neuron whose state exceeds a threshold produces a spike. There's a "noise" generator in the core (pseudo-random number generator) that can add "noise" to spike thresholds and stochastically open synapses. A buffer holds incoming spikes for delayed delivery.

This approach allows for distributing the "knowledge" of signal processing principles across the entire chip simultaneously without separating data and the execution block.

### Conclusion

As mentioned earlier, the idea of neuromorphic computers isn't new; many have attempted to implement this approach for several decades, but now there's a favorable environment for their development. First and foremost, there's an understanding of why this architecture is necessary and what it's needed for. Humanity has created the infrastructure and accumulated an immense amount of data that now needs processing. Secondly, hardware manufacturers have accumulated experience and are ready for complex, non-standard processor architectures. Like von Neumann computers, neuromorphic architecture is designed to solve a specific set of problems. For solving such tasks, this architecture possesses several advantages:

- Scalability
- Computational parallelism
- Energy efficiency
- Ability to process sequences and continuous signals
- High adaptability to signals

Due to the novelty of the technology, such architecture has a downside – the cost of a single chip. More accurately, these chips are simply not yet produced for sale and are created for internal research purposes.

In the next article, I'll demonstrate how to create a primitive network using a simulator and process various signals with it.

### References

[1] J. Von Neumann and R. Kurzweil, The computer and the brain. Yale University Press, 2012.

[2] A. M. Turing, “Computing machinery and intelligence,” Mind, vol. 59, no. 236, pp. 433–460, 1950. 

[3] nanoCMOS Device, Circuit and System Simulations, https://cnx.org/contents/hMLR8R0g@1/nanoCMOS-Device-Circuit-and-System-Simulations

[1] J. Von Neumann and R. Kurzweil, The computer and the brain. Yale University Press, 2012.

[2] A. M. Turing, “Computing machinery and intelligence,” Mind, vol. 59, no. 236, pp. 433–460, 1950. 

[3] Types of neurons https://qbi.uq.edu.au/brain/brain-anatomy/types-neurons

[4] Computing complex visual features with retinal spike times Gütig R, Gollisch T, Sompolinsky H, Meister M (2013)

[5] Industrial DVS Design; Key Features and Applications http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Eric_Ryu_Samsung.pdf

[6] Spike-shape dependence of the spike-timing dependent synaptic plasticity in ferroelectric-tunnel-junction synapses https://www.nature.com/articles/s41598-019-54215-w/

[7] Benchmarking Keyword Spotting Efficiency on Neuromorphic Hardware https://arxiv.org/abs/1812.01739

[8] Advancing neuromorphic computing From promise to Competitive technology. https://niceworkshop.org/wp-content/uploads/2019/04/NICE-2019-DAY-2a-Mike-Davies.pdf