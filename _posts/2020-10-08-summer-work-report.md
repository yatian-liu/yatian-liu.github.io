---
layout: post
title: Report for My Summer Work on the Mic Array Project
---

I wrote a [report](/public/PDM_PCM_Signal_Conversion_FPGA.pdf) for my summer
work on the microphone array as a required submission for my summer lab intern.
The report is written in the format of a short conference paper and presents my
part of the work on the microphone array project in detail, so I think it is
worth being put on this website. To summarize, more rigorous tests on the CIC
and the FIR filter's performance were conducted using both simulation and the
real hardware after the FIR filter was working. I started working on the
Ethernet data transmission in mid August but the combined system is still not
working. We can now send and receive constant data using the Triple-Speed
Ethernet IP Core given by Intel, but the data interfaces of the filter and the
Ethernet IP core are quite different so we need to figure out the glue logic
between the two interfaces.
