+++
title = "Frequency domain features"
date = 2020-04-03T12:34:36+13:00
weight = 1
pre = "<b>2.1 </b>"
disableToc = true
+++

### Spectral Flux
Is the measure of the changes in the shape of the spectrum over time. SF is computed as the Euclidean ($L^2$) distance of two consecutive spectral frames with normalised PSD

### Spectral Slope
For many natural audio signals, the energy of the spectrum tends to decrease towards the higher end of the frequency range, the "slope" of which is related to the nature of the sound source. This parameter can be found via linear regression of the magnitude:
$$x(f) = slope \times f + intercept$$
where $x(f)$ is the magnitude function and $f$ is the frequency value. In addition to slope, the intercept and regression error can also be used as features.

### Spectral Centroid
is the centre of gravity of the spectrum, calculated as the weighted mean of the frequencies using their normalised magnitude as weights:

$$SC = \sum_{n=1}^{N} \Big(f(n) \times x(n)\Big) \Bigg/ \sum_{n=1}^{N} x(n)$$

Where $N$ is the total number of frequency bins, $a(n)$ is the normalised magnitude of the spectrum at bin $n$ and $f(n)$ is the centre frequency of bin $n$. Value of SC is the frequency where most of the energy is concentrated in, which is usually where the dominant frequency is found.

### Spectral Centre
Is the frequency where half of the energy in the magnitude spectrum is above and half is below

### Spectral Rolloff
Is defined as the \textit{N}\% percentile of the power spectrum. In practice, the value of \textit{N} is usually at the higher end (85, 95, etc).

Spectral Centre is a Spectral Rolloff with $N=50$

### Spectral Flatness
Also known as **Wiener entropy** is a measure of the noisiness of the spectrum, of which the higher value correspond to a more uniform distribution of power over all frequencies. It is computed as the ratio of the geometric mean over the arithmetic mean of the spectrum:

$$SF = \sqrt[N]{\prod_{n=1}^{N}x(n)} \Bigg/%
\frac{1}{N} \sum_{n=1}^{N}x(n)$$

### Spectral Crest
Is the opposite of **Spectral Flatness**. it measures how peaky the spectrum is. A noisy spectrum have low value of SCF compare to a clear tonal spectrum. It is calculated as the ratio of the peak over the mean frequency value:

\begin{equation*}
SCF = \max_{1 \le n \le N} x(n) \Bigg/ \frac{1}{N} \sum_{n=1}^{N}x(n)
\end{equation*}

### Bandwidth
Also known as **Spectral Spread**, is usually defined as the magnitude-weighted average of the differences between the spectral components and the spectral centroid

\begin{equation*}
BW = \sum_{n=1}^{N} \Big(\big(f(n)-SC\big) \times x(n)\Big) \Bigg/ \sum_{n=1}^{N} x(n)
\label{eq:bandwidth}
\end{equation*}

### Fundamental Frequency
Is the lowest frequency of a harmonic series. It concurs with the rate of oscillation of the sound source. The FF is the same as the dominant frequency in case of pure-tone signals, which makes it relatively straightforward to determine. However, this is not the case with speech and many bird's vocalisations, which produce complex sound (having harmonic structure). The fundamental frequency of a harmonic series can be determined as either the lowest harmonic or more reliably (in the case of missing fundamental) by finding the largest common denominator of the harmonics. 


### Harmonic Ratio
Is the ratio of harmonic power to total power, it is computed in the autocorrelation domain and defined as the maximum value of the normalised autocorrelation function (after having ignored the zero-lag peak) within a frame of length $k$:

\begin{equation*}
HR = \max_k \Bigg(\sum\nolimits_j \Big(s(j)\times s(j-k)\Big) \Big/ \sqrt{\sum\nolimits_j s(j)^2 \sum\nolimits_j s(j-k)^2} \Bigg)
\end{equation*}

Where $s(j)$ is the function of sound pressure in time domain.
