
# Aim
Write a simple Python program for the construction and reconstruction of ideal sampling.
# Tools required
# Program
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
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
 plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()
 reconstructed_signal = resample(signal_sampled, len(t))
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
 plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()

# Output Waveform
<img width="1224" height="507" alt="Screenshot 2025-09-19 103630" src="https://github.com/user-attachments/assets/d2648c0f-d560-44d9-b419-20cc2c2c230d" />
<img width="1146" height="504" alt="Screenshot 2025-09-19 103637" src="https://github.com/user-attachments/assets/3728f283-7295-4fe4-bc14-c8ac2c52b3a4" />
<img width="1114" height="503" alt="Screenshot 2025-09-19 103644" src="https://github.com/user-attachments/assets/76220b13-b1b7-4079-b618-90634c32ba2a" />





Results

Hence Wrote a simple Python program for the construction and reconstruction of idealsampling.

