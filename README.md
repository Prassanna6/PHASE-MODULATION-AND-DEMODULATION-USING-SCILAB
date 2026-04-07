# PHASE-MODULATION-AND-DEMODULATION-USING-SCILAB
AIM

To write a program for Phase Modulation and Demodulation using SCILAB and to observe and measure the phase deviation and modulation index.

APPARATUS REQUIRED

Computer with i3 Processor or higher
SCILAB Software

THEORY

Phase Modulation (PM) is a modulation technique in which the phase of the carrier signal is varied in accordance with the instantaneous amplitude of the modulating signal, while the amplitude of the carrier remains constant.

Phase Deviation (Δφ)

Phase deviation represents the maximum change in phase of the carrier signal.

Δφ = kp * Am

Where:

kp = Phase sensitivity (rad/volt)
Am = Amplitude of modulating signal
Modulation Index (mp)
mp = Δφ

For sinusoidal signals:

mp = kp * Am
PM Signal Equation
s(t) = Ac cos(2πfc t + kp m(t))

For sinusoidal modulating signal:

s(t) = Ac cos(2πfc t + mp sin(2πfm t))

Where:

Ac = Carrier amplitude
fc = Carrier frequency
fm = Modulating frequency
kp = Phase sensitivity
mp = Modulation index

ALGORITHM

Define parameters:
Sampling frequency Fs
Time duration T
Carrier frequency fc
Modulating frequency fm
Phase sensitivity kp
Generate signals:
m(t) = sin(2πfm t)
c(t) = cos(2πfc t)
PM Modulation:
s(t) = cos(2πfc t + kp * m(t))
PM Demodulation:
Differentiate the PM signal
Apply envelope detection:
|s(t)|
Use low-pass filter to recover the original signal
Plot all signals:
Modulating signal
Carrier signal
PM signal
Demodulated signal

PROCEDURE

Refer to the algorithm and write the SCILAB code.
Open SCILAB software.
Create a new script file.
Enter the program and save it.
Execute the code.
Debug errors if any and re-run.
Observe the generated waveforms.

PROGRAM

```
clc;
clear;
close;

Ac = 7.4;          // Carrier amplitude
Am = 3.7;        // Message amplitude
Fc = 1660;        // Carrier frequency
Fm = 166;         // Message frequency
Fs = 16600;       // Sampling frequency
kp = %pi/4;       // Phase sensitivity constant

t = 0:1/Fs:2/Fm;  // Time vector (two cycles of message)

// Message signal
E1 = Am * sin(2*%pi*Fm*t);
subplot(3,1,1);
plot(t, E1);
xlabel("Time (s)");
ylabel("Amplitude");
title("Message Signal");

// Carrier signal
E2 = Ac * sin(2*%pi*Fc*t);
subplot(3,1,2);
plot(t, E2);
xlabel("Time (s)");
ylabel("Amplitude");
title("Carrier Signal");

// Phase Modulated signal
E3 = Ac * sin(2*%pi*Fc*t + kp*E1);
subplot(3,1,3);
plot(t, E3);
xlabel("Time (s)");
ylabel("Amplitude");
title("Phase Modulated Signal");

xgrid();
```

GRAPH 

![WhatsApp Image 2026-04-07 at 9 45 10 PM](https://github.com/user-attachments/assets/8726eb06-07c8-48a7-a203-29eff2f6a75c)


TABULATIONS

<img width="1080" height="672" alt="image" src="https://github.com/user-attachments/assets/02911be7-3e17-4e9a-856a-130196c327d0" />


RESULT

Thus the phase modulation and demodulation is experimentally done and the output is verified.
