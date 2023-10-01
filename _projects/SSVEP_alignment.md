---
title: "EEG-based SSVEP Signal Preprocessing and Analysis"
excerpt: "Preprocessing and analysis of EEG-based SSVEP signal collected from customized electrodes"
teaser: "../images/SSVEP_alignment.png"
date: "2022-09-01"
collection: projects
category: research
tags: [Electrophysiological Sensing, EEG, Data Analysis, Bluetooth ]
links:
---

Offline preprocessing and alignment of SSVEP signal with expected timestamp to achive higher classification accuracy.
![Alignment](../SSVEP_alignment/alignment.png)

To make the signal cleaner, a standard bandpass filter is applied to facilitate the alignent process using scipy sosfiltfilt.

![Bandpass Filter](../SSVEP_alignment/bandpass.png)

The scipy.signal.sosfiltfilt function from the SciPy library is used for filtering data. It performs a forward-backward, zero-phase digital filtering. This function uses a second-order sections (SOS) filter representation, which can provide better numerical accuracy and stability compared to traditional transfer function (ba) representations.

The sosfiltfilt function performs the filtering in two passes: once forward through the data, and once backward, which results in a zero-phase filtering effect. This is a desirable quality because it doesn't introduce any phase distortion into the filtered signal.
