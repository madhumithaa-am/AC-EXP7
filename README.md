# AC-EXP7
# EXPT.NO.7	Phase Modulation

# Aim

To implement and analyze phase modulation (PM) using Sci lab 
 Apparatus Required
1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer Theory
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:



# Algorithm
 
1.	Initialize Parameters:
o	Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).
2.	Generate Time Axis:
o	Create a time vector for the signal duration based on the sampling frequency.
3.	Generate Message Signal:
o	Define the message signal as a cosine wave.
4.	Generate PM Signal:
o	Apply the PM modulation formula to obtain the modulated signal.
5.	Plot the Signals:
o	Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.

# CODE
```
am = 14.57;
fm = 1082;
ac = 29.74;
fc = 10820;
fs = 108200;
t = 0:1/fs:2/fm;
em = am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec = ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);

b = 1.75 + 7*(0.22);
efm = ac*cos(2*3.14*fc*t + b*sin(2*3.14*fm*t));

epm = ac*cos(2*3.14*fc*t + b*cos(2*3.14*fm*t))


subplot(4,1,3);
plot(t,efm);
subplot(4,1,4);
plot(t,epm);

```
# output waveform:

<img width="1917" height="1197" alt="image" src="https://github.com/user-attachments/assets/2c5bc9b1-4d50-4878-b58d-7f8544ff8734" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/235d64c5-ba5a-41c1-9873-d4b628423fd0" />



 
# Result

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
