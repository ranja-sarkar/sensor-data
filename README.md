
Manufacturing industries have evolved over 3 centuries with electrification, automation, and digitalization – from steam to sensor, or Industry 1.0 to Industry 4.0. 

The first industrial revolution (Industry 1.0) was seen with steam engines during the end of 18th century and start of 19th century. Entire 19th century thereafter was Industry 2.0, which experienced mass production (assembly lines) with electric power. In the 20th century, Industry 3.0 saw automated, intelligent production line using electronics and IT. The 21st century saw the advent of digitalization, internet of things (IoT), and [sensors](https://www.advancedtech.com/blog/sensor-data/). Algorithmic computation largely evolved from the period of Industry 3.0 and was put into use.

Industry 4.0 in the 21st century is about smart manufacturing. Artificial Intelligence (AI) started evolving from Industry 3.0 – it’s like only machine learning during Industry 3.0, machine learning alongwith deep learning (neural networks) during Industry 4.0 and GPTs (generative AI) currently are emerging pretty fast as sub-fields of AI. This means connected and integrated systems, huge data sharing via managed cloud services efficiently, which allow manufacturers to respond to customers’ feedback by not compromising on quality etc..  

The adoption of large language models (LLMs) for analysing a customer and his buying behavior is expected to significantly enhance product development and customer experience (his preferences etc.). This enables creation of highly personalized systems. Personalization of integrated plus smart systems would perhaps be next in Industry 5.0 (mid to end of 21st century). 

-----

**Chapter 1** of my [book](https://www.amazon.com/dp/1804616702?ref=cm_sw_r_ffobk_cp_ud_dp_XZZZH4S92PNS2KJB3KVF&ref_=cm_sw_r_ffobk_cp_ud_dp_XZZZH4S92PNS2KJB3KVF&social_share=cm_sw_r_ffobk_cp_ud_dp_XZZZH4S92PNS2KJB3KVF&bestFormat=true) has a portion covered on **signal processing**. Signal processing is the transformation of a signal (measured time-series) to hyper-spectral images. Spectrograms and wavelet transforms are often used as inputs to machine learning algorithms.

An excerpt from my book: 

<img width="422" alt="rs7" src="https://github.com/user-attachments/assets/035623d8-5c24-48cd-870b-4fd82fe5824f" />

The classic Kalman Filter is used in signal processing to produce estimates of unknown (dynamic) variables at each time step using time-series data. It is covered in **Chapter 7** of my book.  However, understanding the fundamentals of a [vibratiion signal](https://blog.endaq.com/top-vibration-metrics-to-monitor-how-to-calculate-them) and analysing it is foremost. Analyzing the trends of vibration metrics would inform decisions for condition-based or predictive maintenance.

-----

# Fast Fourier Transform of time-series signal

Any waveform is actually just the sum of a series of simple sinusoids of different frequencies, amplitudes, and phases.  A Fourier series is that series of sine waves; and we use Fourier analysis or spectrum analysis to deconstruct a signal into its individual sine wave components. 

A fast Fourier transform ([FFT](https://blog.endaq.com/vibration-analysis-fft-psd-and-spectrogram)) is a discrete Fourier transform (DFT) using a more efficient algorithm that takes advantage of the symmetry in sine waves.

<img width="337" alt="12" src="https://github.com/user-attachments/assets/165cd62f-3a0a-4648-942c-1683449e0ace" />
<img width="365" alt="13" src="https://github.com/user-attachments/assets/3698b7ab-1dbd-4226-8cfb-71ef66b041e6" />

As an **example**, we think of an accelerometer that measures engine vibrations or yields vibration signal. By analysing the **vibration data** we can infer whether it is ACTIVE (engine is running and the vehicle is moving), IDLE (engine is running but the vehicle is not moving) or OFF (engine is off), and also test and diagnose machine faults. Such engines can be that of electric vehicles (cars, bikes), or off-highway vehicles (wheeled-loaders, dump trucks, excavators), and others.

<img width="667" alt="rs2" src="https://github.com/user-attachments/assets/41baa0e4-98e4-461d-b1e2-87645ec62dbd" />
<img width="668" alt="rs1" src="https://github.com/user-attachments/assets/256359c2-20f7-4313-9fae-887b4f8ef1ca" />



# Change point detection in time-series data

Changes in signals can take different forms. A change point is an abrupt change in a time-series, meaning a change in the (statistical characteristics) underlying trend, frequencies, or probability distribution.

**Types of change points:**

1. **Change in mean**

One of the earliest algorithms for detecting change in mean is the Cusum algorithm, applied for quality control in manufacturing.
For more: https://sarem-seitz.com/posts/probabilistic-cusum-for-change-point-detection.html

   <img width="404" alt="rs1" src="https://github.com/user-attachments/assets/724a753e-a14f-454c-ac13-8772e9f9149e" />


2. **Change in variance**

   There can be segments in the time-series with different variance values, which appear as sudden noise in the signal. 
   
<img width="389" alt="rs2" src="https://github.com/user-attachments/assets/68e11498-94fe-4689-8d7d-fb121684272d" />

3. **Change in periodicity/frequency**

Detection of this kind of change is typically done in the frequency (not time) domain of the signal, for example by  using Fourier transform or Wavelet transform.   

   <img width="410" alt="rs3" src="https://github.com/user-attachments/assets/a14a791b-4a1d-40f5-8737-f9fe773d3d2a" />


4. **Change in pattern**

To detect this kind of change is harder than the previous ones. 

Change point detection seems to be closely related to anomaly detection; the difference between the two tasks is sometimes unclear.

  <img width="399" alt="rs4" src="https://github.com/user-attachments/assets/4fb80be4-9a95-40aa-b49b-20ecb7bd7e14" />


**Commonly used python packages/libraries for change point detection:** are [ruptures](https://centre-borelli.github.io/ruptures-docs/), [sktime](https://github.com/sktime/sktime), and [luminaire](https://zillow.github.io/luminaire/tutorial/dataprofiling.html)

# References

1. [Change-point detection in time-series via deep learning](https://academic.oup.com/jrsssb/article/86/2/273/7517020)

2. [A survey of methods for time-series Change Point Detection](https://pmc.ncbi.nlm.nih.gov/articles/PMC5464762/)


 

   



