# Ideal, Natural, & Flat-top -Sampling
# Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
# Tools required
# Program
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample

fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)

plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()

t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)

plt.figure(figsize=(10, 4))
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()

reconstructed_signal = resample(signal_sampled, len(t))

plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()

```
# Output Waveform
# Ideal Sampling
<img width="989" height="889" alt="image" src="https://github.com/user-attachments/assets/f4d5b4d1-a0c4-4168-b23b-ab38ec692b90" />

# Natural Sampling
<img width="1390" height="989" alt="image" src="https://github.com/user-attachments/assets/e0c17098-ba63-4208-88e6-d04055974e48" />

# Flat-top Sampling
<img width="1398" height="990" alt="image" src="https://github.com/user-attachments/assets/ca9b1dcf-894b-4ae4-b27e-077c52ae2d16" />

# Results
Thus we consrtucted and reconsrtucted ideal, natural and flat top sampling using python code.
# Hardware experiment output waveform.
