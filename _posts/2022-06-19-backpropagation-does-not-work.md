---
layout: post
title: "Backpropagation does not work"
subtitle: "Backward error distribution technique not applied for big and complex systems."
date: 2022-06-19 18:15:00 +0300
background: '/img/posts/2022-06-19/backpropagation.jpg'
---
One of the major roles in modern artificial intelligence algorithms taken by artificial neural networks. Its idea is based on simulating neurons in some approximation. The artificial neural network learning process is possible by backward error propagation but that approach is not good enough for really deep neural networks. 

First of all it is because the error value is taking too less effect on first layers. You need to push over too many examples to get enough valuable changes in the first layers  of the network.
It is difficult to imagine that our brain is using end level result to tune your motor actions.

The second point is physiological. Backpropagation is propagation of error value in opposite direction of the main signal propagation direction. It means the brain’s neural network must contains a huge number of neurons which can send signals from some resolution point to the front networks. 

REFERENCES
1. Geoffrey E. Hinton, James L. McClelland "Learning representations by recirculation" NIPS 358, (1987). [PDF](/downloads/posts/2022-06-19/NIPS-1987-learning-representations-by-recirculation-Paper.pdf) 
2. Geoffery Hinton, "Can sensory cortex do backpropagation?", [Part of a symposium to celebrate the work of Professor Sir David MacKay FRS. The symposium was held over the period 14-15 March 2016.](http://divf.eng.cam.ac.uk/djcms2016/) [Video](https://www.youtube.com/watch?v=cBLk5baHbZ8)