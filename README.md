# exercise13
###Abstract

Here in this assignment, we will look into the function in which time is a value of interest as well as the space vairables. First, we'll investigate the simplest condition--on dimensioin condition, the propagation of waves on a string, and then consider the 2 dimension situation--the vibration of a menbrane.

***
###Background

The central equation of wave motion is:

<img src="http://latex.codecogs.com/gif.latex?\frac{\partial^{2}y}{\partial(t)^{2}}=c^{2}\frac{\partial^{2}y}{\partial(x)^{2}}" alt=""title="" />

Which is usually referred to as the wave equation. This equation could be solved numerically by the following solution:

<img src="http://latex.codecogs.com/gif.latex?\frac{d^{2}y_{i}}{dt^{2}}=(T\div\mu)\frac{y_{i+1}-2y_{i}+y_{i-1}}{\Delta(x)^{2}}\approx(T\div\rho)\frac{\partial^{2}y}{\partial(x)^{2}}" alt=""title="" />

This equation could be written in this form:

<img src="http://latex.codecogs.com/gif.latex?\frac{y_{i,n+1}+y_{i,n-1}-2y_{i,n}}{\Delta(t)^{2}}\approx(c)^{2}\frac{y_{i+1,n}+y_{i-1,n}-2y_{i,n}}{\Delta(x)^{2}}" alt=""title="" />

So we can get:

<img src="http://latex.codecogs.com/gif.latex?y_{i,n+1}=2[1-r^{2}]y_{i,n}-y_{i,n-1}+r^2[y_{i+1,n+1}+y_{i-1,n}]}" alt=""title="" />

<img src="http://latex.codecogs.com/gif.latex?r=\frac{\Delta(t)}{\Delta(x)}" alt=""title="" />

We usually chose r=1 in calculation, when it comes to the composite string, r can be a bit smaller than 1. n is the time step while i is the position step.

Then comes to the 2 dimension condition. Like the 1d situation, the wave equation could be expressed as:

<img src="http://latex.codecogs.com/gif.latex?\frac{\partial^{2}z}{\partial(t)^{2}}=c^{2}(\frac{\partial^{2}z}{\partial(x)^{2}}+\frac{\partial^{2}z}{\partial(y)^{2}})" alt=""title="" />

And we can rewrite it into:

<img src="http://latex.codecogs.com/gif.latex?\sigma\Delta(x)\Delta(t)\frac{\partial^{2}z_{k}}{\partial(t)^{2}}=T(z_{k+1}+z_{k-1}+z_{k+N}+z_{k-N}-4z_{k})" alt=""title="" />
 
Solve it, and we will obtain:

<img src="http://latex.codecogs.com/gif.latex?z_{k}=A_{k}e^{-i\omega(t)}" alt=""title="" />


<img src="http://latex.codecogs.com/gif.latex?\frac{\omega^{2}T\sigma\Delta(x)\Delta(y)}{T}\vec{A}=D\cdot\vec(A)" alt=""title="" />

D is the dynamic matrix, omega is the frequency. 

***
###Exercise

####step one: the propagatioin of wave

First, let's talk about the ideal string. We have assumed the 'Gaussian pluck' of the string.

![img](https://github.com/LuxAsteria/test3/blob/master/stirngsiml.gif)

If the string is composite, it  will vibrate dramaticly when it traval across the connected point.

![img](https://github.com/LuxAsteria/test3/blob/master/stirngcomps.gif)

To solve the problem, we can set the values of r of both string the same, and change delta x, and at this time the move of wave will be smooth.

![img](https://github.com/LuxAsteria/test3/blob/master/stirngcomps%20pro.gif)

[For code please click here](https://github.com/LuxAsteria/exercise13/blob/master/code)
***

####step two: the spectrum

First, let's see the signal 5 percent off the end of the string.

![img](https://github.com/LuxAsteria/test3/blob/master/signal.png)

Based on the periodic behaviour of the string, we can print the power spectrum of it.The first one is the spectrum of string excited 5 percent from the center while the second one was excited 7 percent from its center.

![img](https://github.com/LuxAsteria/test3/blob/master/spectrum%200.5.png)

![img](https://github.com/LuxAsteria/test3/blob/master/spectrum0.7.png)

[For code please click here](https://github.com/LuxAsteria/exercise13/blob/master/code)
***
####step three: the vibration of menbrane

Here's the pircture of menbrane at different times.

![img](https://github.com/LuxAsteria/test3/blob/master/menbran1.png)

![img](https://github.com/LuxAsteria/test3/blob/master/menbrane2.png)

![img](https://github.com/LuxAsteria/test3/blob/master/menbrane3.png)

![img](https://github.com/LuxAsteria/test3/blob/master/menbrane4.png)

[For code please click here](https://github.com/LuxAsteria/exercise13/blob/master/code)
***
###Conclusion
The vibration of a string, and, what's more, a menbrane is a really interesting thing to investigate. When it comes to higher dimensions, the movement should be described by more complex tensor. For one dimension movement, it could be dipicted with a constant, or a number, but in 2 dimension, it should be enumerated using matrix.
***
###Acknowledge

[1]Computational Physics, Edition 2, Nicholas J.Giordano 


##PS:All Rights Reserved
