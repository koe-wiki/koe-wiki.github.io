+++
title = "Time domain features"
date = 2020-04-03T12:34:36+13:00
weight = 2
pre = "<b>2.2 </b>"
disableToc = true
+++

The time domain represents changes in the signal over time, or more precisely, the changes in air pressure when the sound reaches a microphone, which is measured by voltage value. Features in this category are necessarily extracted directly from the oscillogram without any transformation. Thus, they tend to have excellent time resolution and low computational cost.

### Zero Crossing Rate (ZCR)
Defined as the number of zero crossings within one second is an efficient way to approximate the dominant frequency


### Temporal Envelope
Is the smoothed amplitude calculated by a moving window over the absolute value of the signal's waveform. For signals that have relatively low and constant background noise, the temporal envelope provides a simple way to detect intervals of silence and thus could be used for audio segmentation.

### Short-time energy
Is the mean square of the amplitude of the waveform over one frame

$$p\triangleq\frac{\sum_{i=t}^{t+d-1} {s_i}^2}{d}$$

### Loudness
Is the root mean square of the amplitude of the waveform over one frame

$$p\triangleq\sqrt{\frac{\sum_{i=t}^{t+d-1} {s_i}^2}{d}}$$

### Temporal Centroid
Is the point in time where most of the signal energy is concentrated, calculated as the time average over the envelope of a signal in seconds

### Log Attack Time
is the logarithm of time duration from the beginning of the sound to the point where the envelope reaches its first maximum. LAT characterises the attack of sound, which can be smooth or sudden.