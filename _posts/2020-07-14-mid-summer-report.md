---
layout: post
title: Mid-Summer Report for the Microphone Array Project
---

This is my report for the work I have done for the microphone array project
after half of the summer vacation has passed and what I plan to achieve in the
rest of the summer.

## What I have done
At the beginning of May, I was admitted to the SPQR Lab for the microphone array
project. In the first two weeks, I read two papers about microphone arrays and
knew the basic structure of it: PDM microphones, CIC and FIR filters, and
on-FPGA circuits or PC programs for beamforming. After that, I made my
rudimentary personal website, which is this website. Since it is my first time
making a website by writing code, it took me several days to set it up, but it
was time well spent. In the following month, I mainly worked on the CIC filter
and the FIR filter. I first learned how to use the Quartus Prime software for
FPGA development with the help of Julia. It is a large and versatile software,
and I am still learning new features of it. Then, I tried to get the CIC filter
working. I learned about the structure and frequency response of the filter and
did a presentation for my study, which gave me a much deeper understanding of
the filter than before. I also reviewed EECS 216's content to better understand
digital signal processing. To test the filter's functionality, I first used a
sine wave file given by Julia as input signal and then wrote a MATLAB script to
generate a sine wave sweep as input under the advise of Prof. Alanson Sample.
The debugging process took considerable time, but finally the CIC filter works
as expected now. The FIR compensation filter is also added and debugged, but all
my current tests are simulations, so I am working on connecting the microphone
to the FPGA board and upload the program to see the filter's real world
performance.

## What I plan to do
Since the filtering part is almost done, I believe I can get the physical
microphone with filters work in this week, hopefully by today. After this part,
there is still plenty of work to be done. I need to work together with Sarthak
for the data transmission part, and I also need to adjust the parameters of the
filters to match the microphone arrays we are going to use instead of the
testing microphone I am using now. Once the program works for the microphone
array, the beamforming development can be started. It may take considerable time
and thus may not be finished by the end of the summer. If I could continue
working on the project after the fall semester starts, I could help with
exploring the applications of the microphone array when the beamforming is done.
