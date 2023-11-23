---
layout: post
title: "Backpropagation does not work"
subtitle: "Backward error distribution technique not applied for big and complex systems."
date: 2022-06-19 18:15:00 +0300
background: '/img/posts/2022-06/backpropagation.jpg'
---
A significant role in contemporary artificial intelligence algorithms is played by artificial neural networks, built around the concept of approximating neurons. While the learning process in these networks is enabled through backward error propagation, this method proves inadequate for extremely deep neural networks.

One primary challenge lies in the minimal impact of error values on the initial layers. To effect meaningful changes in these early layers, an extensive number of examples must be processed, making it hard to conceive that our brains fine-tune motor actions using solely end-level outcomes.

Another aspect involves physiology. Backpropagation involves the propagation of error values in the opposite direction of the primary signal. Consequently, the brain's neural network must house an immense number of neurons capable of transmitting signals from specific resolution points to the preceding networks.

REFERENCES
1. Geoffrey E. Hinton, James L. McClelland "Learning representations by recirculation" NIPS 358, (1987). [PDF](/downloads/posts/2022-06-19/NIPS-1987-learning-representations-by-recirculation-Paper.pdf) 
2. Geoffery Hinton, "Can sensory cortex do backpropagation?", [Part of a symposium to celebrate the work of Professor Sir David MacKay FRS. The symposium was held over the period 14-15 March 2016.](http://divf.eng.cam.ac.uk/djcms2016/) [Video](https://www.youtube.com/watch?v=cBLk5baHbZ8)