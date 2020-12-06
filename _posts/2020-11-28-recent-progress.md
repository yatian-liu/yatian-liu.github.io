---
layout: post
title: Recent Progress on the Mic Array Project - Ethernet
---

After a long expedition I finally got the Ethernet subsystem working together
with the filter subsystem! I wrote a finite state machine for storing the data
from the filters into a RAM that is accessible by Intel's soft CPU core called
Nios II, and modified the C code given for the Ethernet IP core to send the data
in the RAM to the Ethernet IP core's TX data line. The Ethernet IP core only
supports layer 2 (i.e. data link layer) of the TCP/IP stack and using the full
TCP/IP stack requires a full operating system, which introduces large overhead.
Since our application of sending data from microphone to a computer has tight
timing constraints (the data transmission rate must be higher than the data
generation rate), I decided to run the C code on bare metal to speed up the data
handling process and manually add UDP and IP headers. Interrupts are fired when
new data come in so that the soft CPU core can collect the new data efficiently.
There are some subtleties to deal with and I work part-time on the project after
the Fall semester began so the progress was slow, but finally it is done.

The current system is tested on a two-microphone setup. For the next steps, our
group is considering testing the system on a microphone array we have, and then
try to train the working microphone array for sound source localization using
machine learning methods. We will try various ways of training, for instance
end-to-end training and pre-processing like beamforming.
