# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Blackman Window Sequence 
n=0:1:N-1; 
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1)) 
hn=hd.*wh 
% Plot the Low Pass Filter with Blackman Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'ms');
title('Low Pass FIR Filter using Blackman Window');

```

## OUTPUT:
<img width="695" height="521" alt="image" src="https://github.com/user-attachments/assets/5e3e67dc-7cd1-43db-948d-fe153c5b987d" />


## RESULT:
<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/e511c0cb-c642-45fe-a8ea-e4fd1d3a5a85" />

