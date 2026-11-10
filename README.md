# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
clc;

clear;

xn=[1 2 3 4 4 3 2 1];

n1=0:1:length(xn)-1;

subplot(3,1,1);

plot2d3(n1,xn);

xlabel('Time n');

ylabel('Amplitude xn');

title('Input Sequence');

j=sqrt(-1);

N=length(xn);

Xk=zeros(1,N);

for k=0:N-1

for n=0:N-1

Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);

end

end

disp(Xk)

K1=0:1:length(Xk)-1;

magnitude=abs(Xk)

subplot(3,1,2);

plot2d3(K1,magnitude);

xlabel('frequency(Hz)');

ylabel('magnitude(gain)');

title('magnitude spectrum');

angle = atan(imag(Xk),real(Xk))

subplot(3,1,3);

plot2d3(K1,angle);

xlabel('frequency(Hz)');

ylabel('Phase');

title('Phase spectrum')

### CALCULATIONS:
<img width="900" height="1447" alt="image" src="https://github.com/user-attachments/assets/86e88f88-d612-4b53-8a52-9cfec419e177" />
<img width="900" height="1406" alt="image" src="https://github.com/user-attachments/assets/935493da-a9f4-4ba5-8339-d1d709b002ef" />
<img width="900" height="1432" alt="image" src="https://github.com/user-attachments/assets/67a24f12-dbe5-4892-b479-9c6027e3ba04" />
<img width="900" height="1324" alt="image" src="https://github.com/user-attachments/assets/2a8b077d-3365-4aec-8bea-901523d5f092" />
<img width="877" height="954" alt="image" src="https://github.com/user-attachments/assets/4ab0a03d-0200-4716-b42a-f97972b1c8ce" />

### SAMPLE OUTPUT:
<img width="802" height="491" alt="image" src="https://github.com/user-attachments/assets/ada9ff37-84a1-4585-b81a-cd0697d78b3c" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

