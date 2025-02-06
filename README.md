# Signal processing

An accelerometer measures engine vibrations. By analysing the **vibration data** we can infer whether it is ACTIVE, IDLE or OFF, and also test and diagnose machine faults.
The egines are that of excavators, wheeled-loaders, dump trucks etc.

<img width="466" alt="12" src="https://github.com/user-attachments/assets/c36ca8ed-8831-4070-994a-52470f7917fe" />


IDLE -> engine is running but the vehicle is not moving.

ACTIVE -> engine is running and the vehicle is moving.

OFF -> engine is off

**Fast Fourier Transform (FFT)** of vibration signal:

<img width="337" alt="12" src="https://github.com/user-attachments/assets/165cd62f-3a0a-4648-942c-1683449e0ace" />
<img width="365" alt="13" src="https://github.com/user-attachments/assets/3698b7ab-1dbd-4226-8cfb-71ef66b041e6" />

Useful blogs: 

https://blog.endaq.com/vibration-analysis-fft-psd-and-spectrogram

https://blog.endaq.com/top-vibration-metrics-to-monitor-how-to-calculate-them

**Change point detection in time-series data:**

Changes in signals can take different forms. A change point is an abrupt change in a time-series, meaning a change in the underlying trend, frequencies, or probability distribution.

**Types of change points:**

1. **Change in mean**

   <img width="404" alt="rs1" src="https://github.com/user-attachments/assets/724a753e-a14f-454c-ac13-8772e9f9149e" />


3. **Change in variance**
   
<img width="389" alt="rs2" src="https://github.com/user-attachments/assets/68e11498-94fe-4689-8d7d-fb121684272d" />

5. **Change in periodicity/frequency**

   <img width="410" alt="rs3" src="https://github.com/user-attachments/assets/a14a791b-4a1d-40f5-8737-f9fe773d3d2a" />


7. **Change in pattern**

  <img width="399" alt="rs4" src="https://github.com/user-attachments/assets/4fb80be4-9a95-40aa-b49b-20ecb7bd7e14" />

  # TO BE CONTINUED ..
 

   



