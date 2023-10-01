---
title: "ECG Front End Design - ADS chip selection and design pipeline"
excerpt: "A electrophysiological sensing front-end using TI electriphysiology frontend chip with bluetooth protocol enabled by nRF52 series"
teaser: "../images/ecg_frontend.png"
date: "2023-06-05"
collection: projects
category: research
tags: [ PCB, Electrophysiological Sensing, ECG, Bluetooth ]
links:
---

Comprehensive trial on using Texas Instrument produced electrophysiological ampifier to build frontend that collect bio-signals.

Some key design note and personal reflection during design process.

![Driven Right leg with WCT circuit](../ECG_Frontend/driven-right-leg.png)

This chip use the driven right leg circuit to do common-mode rejection. Where in my previous project, I use driving right leg, which is a novel variation to DGL circuit.

The chip is not efficient - it use a external oscillator in the design, which cause extra space coverage on the PCB board, as well as a noisy coupling caused by the oscillator. In this process, I refreshed my mind on calculation of loading capacitance.

![Loading Capacitance](../ECG_Frontend/loading_capacitance.png)