# SSB

# EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

# AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

# EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


# Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


# PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

# Model Waveform

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

# Program
```
ac=37.6; 
Am=28.6; 
fc=7660;
fm=910;
fs=25000; 
t=0:1/fs:2/fm; 
wc=2*3.14*fc;
wm=2*3.14*fm;
e1=(Am*sin(wm*t));
subplot(4,1,1);
plot(t,e1); 
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal m(t)");
e2=(ac*sin(wc*t)); 
subplot(4,1,2); 
plot(t,e2);
xlabel("Time(s)");
ylabel("Amplitude");
title("Carrier Signal c(t)");
sbsc1=(Am/2.*cos(wc*t-wm*t))-(Am/2.*cos(wc*t+wm*t));
sbsc2=(Am/2.*cos(wc*t-wm*t))+(Am/2.*cos(wc*t+wm*t)); 
e3=(sbsc2)+(sbsc1); 
subplot(4,1,3);
plot(t,e3);
xlabel("Time(s)");
ylabel("Amplitude");
title("SSB-SC Modulated Signal (LSB)");
e4=(sbsc2)-(sbsc1); 
subplot(4,1,4); 
plot(t,e4);
xlabel("Time(s)");
ylabel("Amplitude");
title("SSB-SC Modulated Signal (USB)");
xgrid;
```


# OUTPUT WAVEFORM

<img width="762" height="573" alt="image" src="https://github.com/user-attachments/assets/6ebc769c-67a3-4caf-98c0-1aac29a0d2ac" />

#TABULATION
![WhatsApp Image 2025-09-29 at 16 16 01_d5029ef5](https://github.com/user-attachments/assets/5cfb755f-eeb4-4508-bb40-bde074d2f73b)
![WhatsApp Image 2025-09-29 at 16 16 35_b5011e51](https://github.com/user-attachments/assets/a980ed6a-1c62-4696-849d-d0b1650ba6c0)


# RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





