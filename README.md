# Signal processing

It deals with the transformation of a signal from time-series to hyper-spectral images, which are obtained from different electromagnetic measurements. Spectrograms and wavelet transforms are often used in machine learning as input data. 

The **Chapter 1** of my book has a small portion covered on **signal processing**.

<img width="176" alt="rs5" src="https://github.com/user-attachments/assets/0b22cd8b-bf5d-4e5c-9796-b689c2476131" />

Buy from Amazon: https://a.co/d/2kE7aeq

An excerpt from my book: 

<img width="422" alt="rs7" src="https://github.com/user-attachments/assets/035623d8-5c24-48cd-870b-4fd82fe5824f" />

The classic Kalman Filter is used in signal processing to produce estimates of unknown (dynamic) variables at each time step using time-series data. It is covered in **Chapter 7** of my book. 

However, understanding the fundamentals of a signal and analysing it is foremost which to an extent is covered in this repo. 

**Fast Fourier Transform (FFT)** of vibration signal:

<img width="337" alt="12" src="https://github.com/user-attachments/assets/165cd62f-3a0a-4648-942c-1683449e0ace" />
<img width="365" alt="13" src="https://github.com/user-attachments/assets/3698b7ab-1dbd-4226-8cfb-71ef66b041e6" />

Useful blogs: 

https://blog.endaq.com/vibration-analysis-fft-psd-and-spectrogram

https://blog.endaq.com/top-vibration-metrics-to-monitor-how-to-calculate-them

As an example, we think of an accelerometer that measures engine vibrations. By analysing the **vibration data** we can infer whether it is ACTIVE, IDLE or OFF, and also test and diagnose machine faults.
Such engines can be that of electric vehicles (cars, bikes), or off-highway vehicles (wheeled-loaders, dump trucks, excavators), and others.

<img width="667" alt="rs2" src="https://github.com/user-attachments/assets/41baa0e4-98e4-461d-b1e2-87645ec62dbd" />
<img width="668" alt="rs1" src="https://github.com/user-attachments/assets/256359c2-20f7-4313-9fae-887b4f8ef1ca" />

[IDLE -> engine is running but the vehicle is not moving; ACTIVE -> engine is running and the vehicle is moving; OFF -> engine is off]



**Change point detection in time-series data**

Changes in signals can take different forms. A change point is an abrupt change in a time-series, meaning a change in the (statistical characteristics) underlying trend, frequencies, or probability distribution.

**Types of change points:**

1. **Change in mean**

One of the earliest algorithms for detecting change in mean is the Cusum algorithm, applied for quality control in manufacturing.
For more: https://sarem-seitz.com/posts/probabilistic-cusum-for-change-point-detection.html

   <img width="404" alt="rs1" src="https://github.com/user-attachments/assets/724a753e-a14f-454c-ac13-8772e9f9149e" />


3. **Change in variance**

   There can be segments in the time-series with different variance values, which appear as sudden noise in the signal. 
   
<img width="389" alt="rs2" src="https://github.com/user-attachments/assets/68e11498-94fe-4689-8d7d-fb121684272d" />

5. **Change in periodicity/frequency**

Detection of this kind of change is typically done in the frequency (not time) domain of the signal, for example by  using Fourier transform or Wavelet transform.   

   <img width="410" alt="rs3" src="https://github.com/user-attachments/assets/a14a791b-4a1d-40f5-8737-f9fe773d3d2a" />


7. **Change in pattern**

  <img width="399" alt="rs4" src="https://github.com/user-attachments/assets/4fb80be4-9a95-40aa-b49b-20ecb7bd7e14" />

  # TO BE CONTINUED ..
 

   



