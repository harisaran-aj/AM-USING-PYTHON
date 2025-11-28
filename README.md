# AM-using-Python

## Aim
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:


## Algorithm

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=6.5
fm=577
Ac=13
fc=577
fs=57700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,s)
plt.show()

```
## Output Waveform

<img width="728" height="527" alt="image" src="https://github.com/user-attachments/assets/eade7878-d736-4c01-a719-cc6693921fcb" />

## Tabular Column


![WhatsApp Image 2025-11-29 at 00 53 25_a76cb2d0](https://github.com/user-attachments/assets/d368c9ee-ea86-4284-9d40-a41f57da6942)


## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots.
The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
