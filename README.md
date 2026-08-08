
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION
```asm
clc;
clear;
x = [10 10 10 10];
h = [2 4 6 8];
m = length(x);
n = length(h);
a = 0:m-1;
b = 0:n-1;
subplot(3,1,1);
plot2d3(a, x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b, h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
y = zeros(1, m+n-1);
for i = 1:(m+n-1)
conv_sum = 0;
for j = 1:i
if ((j <= m) & ((i-j+1) <= n))
conv_sum = conv_sum + x(j) * h(i-j+1);
end
end
y(i) = conv_sum;
end
disp(y, 'Convolution Sum using Direct Formula Method = ');
subplot(3,1,3);
t = 0:(m+n-2);
plot2d3(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Output Signal y');

```

### CALCULATIONS:





### SAMPLE OUTPUT:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2169adf9-292c-446f-add9-6286fbcd6e2d" />




RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
