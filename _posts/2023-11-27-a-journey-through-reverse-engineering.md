---
layout: post
title: "A Journey Through Reverse Engineering"
subtitle: "Unveiling the Quest for Personalized Wearable Tech: A Journey Through Reverse Engineering"
date: 2023-11-27 22:00:00 +0300
background: '/img/posts/2022-07/background_5.jpg'
---
### Unveiling the Quest for Personalized Wearable Tech: A Journey Through Reverse Engineering
![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/casio-g-shock.jpg "Reverse Engineering CASIO GBD-200")

I've been exploring the world of modern wearable devices, but I find them lacking in a crucial aspect: battery life. To me, the ideal wearable should last for months without needing a charge. Unfortunately, the market doesn't offer a device that fits my criteria; they come with unnecessary features and don't prioritize what's truly important.

So, I've decided to create my own. I don't have the time to start from scratch with hardware design, but I found a potential fit in the [CASIO GBD-200](https://www.casio.com/intl/watches/gshock/product.GBD-200UU-9/). However, its software isn't up to par for my needs.

### Tear-down

My initial plan was a tear-down to identify the microcontroller and gather necessary datasheets. The process was straightforward—easy disassembly without extra parts. But there was a setback: the microcontroller lacked any identifiable label.

![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/IMG_3260.png "Tear-down CASIO GBD-200")

![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/IMG_3263.png "Tear-down CASIO GBD-200")


### Nordic Semiconductor dongle to sniff traffic

Moving on to step two, I used a Nordic Semiconductor dongle and Wireshark to intercept data between the CASIO device and iOS app. While I could capture the communication protocol, it didn't yield the firmware I sought. There were no clues about the manufacturer either.

![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/Nordic.png "Nordic Semiconductor dongle")

### Reverse Engineering of iOS app communication protocol

Step three led me to explore the iOS application. By intercepting traffic between the app and CASIO servers, I aimed to uncover requests for new firmware. After some maneuvering with reverse proxy and fake Root CA certificates, I made progress. However, what I discovered was unsettling—CASIO continuously gathers analytics and data about users, which goes against my principles. This motivated me further to develop my own secure firmware for a device I wear constantly.

![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/burp.png "Burp proxy intereptor")


After some additional time, I finally obtained a significant breakthrough—a hint about the microcontroller's name in one of the requests. This led me to a wealth of resources online: guides, datasheets, SDKs, and more. Not a bad outcome for just a couple of hours of reverse engineering.

![Reverse Engineering CASIO GBD-200](https://octadero.com/img/posts/2023-11/reverse-engineering/da14531.png "Burp proxy intereptor")

My next steps involve defining the microchip layout and designing connectors for the available ground connectors on the watch PCB. When I have a free chunk of three hours, I plan to delve deeper. My past experience with light freeROST firmwares should come in handy for this project.
