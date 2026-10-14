# Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]

Due to the high compression ratio of linear frequency modulation (LFM) signals, when implementing active noise interference on these signals, the interference power at the radar receiver input must be multiples of the compression ratio. 
This requires the interference machine to have a high power level. Frequency-hopping interference utilizes the strong coupling between the distance and Doppler frequency of LFM pulse compression radar echo signals, without requiring a high signal-to-noise ratio (SNR), to achieve effective pseudo target interference. 
The principle of linear frequency modulation pulse compression involves the radar transmitting signal's carrier frequency being modulated in a linear manner within the pulse width to achieve broadband signal bandwidth expansion over a large time span. When receiving the echo signals, a match filter is used to compress each echo pulse. This method enables a reasonable compromise between radar operational range, peak power, and resolution. 
The expression for a rectangular pulse linear frequency modulation signal is: 
The frequency domain plot of a linear frequency modulation signal is shown in Figure 1, where T = 30μs, B = 20MHz. It can be seen that the linear frequency modulation signal has an approximate rectangular amplitude characteristic, with a larger B value approaching a rectangle more closely, and its spectral width approximately equaling the modulation frequency deviation B. 
After receiving the echo signals from the radar receiver, the matched filter is used for pulse compression processing. The response function of the matched filter for the input signal s(t) is:
\n        \n  
\n        \n  
\n        \n  
According to equation (8), the pulse-compressed waveform is a narrow pulse in the form of sinx/x, as shown in Figure 2. The width between the main lobe's two nulls is 2/B (in this figure, it is 0.1μs). At -3 dB, the width is approximately 1/B, and the pulse width of the backscatter signal after compression is reduced by BTB times compared to before compression. The peak power of the backscatter signal relative to before compression increases by BTB times. This is the processing gain of linear frequency modulation pulse compression radar.
\n        \n  
Principle of frequency shifting interference\n        \n      \n        \n      \n        \n      \n        \n  
MATLABCode and Simulation Results%%%%%%%%%% Shift frequency interference %%%%%%%%\nclear all;close all;clc;\n​\n%%%%%LFM Signal%%%%%%%%%%%%%%%%%\nT=20e-6;      % Pulse width is 50us\nB=10e6;        %LFM signal bandwidth\nf0=0;      % Intermediate frequency signal\nK=B/T;        % Frequency modulation slope\nfs=40e6;\nts=1/fs;\nSampleNum=T*fs;\n​\nt=linspace(0,T,SampleNum);\nSt=(1/sqrt(T))*exp(j*pi*K*t.^2+j*2*pi*f0*t);\nHt=(1/sqrt(T))*exp(-j*pi*K*(T-t).^2+j*2*pi*f0*(t-T));\n​\nfigure,plot(t,real(St));\nxlabel('Time-s');\nylabel('Amplitude-v');\ntitle('LFMSignal');\n  

## Images

![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](01.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](02.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](03.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](04.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](05.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](06.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](07.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](08.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](09.png)
![Research on Frequency Shifting Interference of Linear Frequency Modulated Pulse Radar [with MATLAB Code]](10.png)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
