---
title: '[Control System] 06 제어공학 Time Response'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
use_math: true
tags: [control_system]
---

# 06 제어공학 Time Response
## Time Response (Transient Response)
[Time Response](/assets/images/Control_System_img/6-1-time-response.jpg)  

specification  
* transient response -> step function (얼마나 빨리 반응 하는지)  
	$R(s)={1 \over s}, \, u(t)$  
* stability  
* steady state error  

System  
* 1st order  
* 2nd order  
* high order  

## First order system  
![First order system](/assets/images/Control_System_img/6-2-first-order-system.jpg)  

## Second order system  
![Second order system](/assets/images/Control_System_img/6-3-second-order-system.jpg)  

### 1. Two distinct real roots  
![Two distinct real roots](/assets/images/Control_System_img/6-4-two-distinct-real-roots.jpg)  

### 2. Repeated real roots  
![Repeated real roots](/assets/images/Control_System_img/6-5-repeated-real-roots.jpg)  

### 3. Complex conjugate roots  
![Complex conjugate roots](/assets/images/Control_System_img/6-6-complex-conjugate-roots.jpg)  

### 4. Pure imaginary roots   
![Pure imaginary roots](/assets/images/Control_System_img/6-7-pure-imaginary-roots.jpg)  

### General 2nd-order system  
![General 2nd-order system](/assets/images/Control_System_img/6-8-general-2nd-order-system.jpg)  

### Underdamped 2nd-order system  
![Underdamped](/assets/images/Control_System_img/6-9-underdamped-2nd-order-system.jpg)  
$(0<\zeta<1)$ step response ->transient response  
$$C(s)={ { { \omega_n}^2}\over{s^2+2\zeta\omega s+{\omega_n}^2} } \cdot {1\over s}={1 \over s} - { {(s+\zeta\omega_n)+{\zeta\over{\sqrt{1-\zeta^2} } } \omega_n \sqrt{1-\zeta^2} } \over {(s+\zeta \omega_n)^2+{\omega_n}^2 (1-\zeta^2)} }$$  
inverse Laplace transform  
$$c(t)=1-e^{-\zeta \omega_n t}(\cos{\omega_n \sqrt{1-\zeta^2} t}+ {\zeta \over \sqrt{1-\zeta^2} } \sin{\omega_n \sqrt{1-\zeta^2} } )$$  
*  $T_p$ (peak time): time required to reach the 1st peak  
	$T_p = {\pi \over \omega_n \sqrt{1-\zeta^2} }$  
* % OS (percent overshoot): ${\text{overshoot}-\text{steady state}\over{\text{steady state} } }\times 100$  
	$\% \text{OS}={C(T_p)-1\over 1}\times 100=100e^{-{\zeta \pi \over \sqrt{1-\zeta^2} } }$  
* $T_s$ (settling time): steady state 2% 머무는데 걸리는 시간  
	$T_s={\ln(0.02\sqrt{1-\zeta^2} ) \over -\zeta\omega_n}$  
  

### Transient response 고려해 제어기 설계  
![Transient response](/assets/images/Control_System_img/6-10-transient-response.jpg)  
  
## High order system
(pole or zero 추가)  
### Pole 추가  
![pole 추가](/assets/images/Control_System_img/6-11-1-pole.jpg)
* case1) $\alpha_r>\zeta\omega_n$ but $\alpha\approx\zeta\omega_n$ 2nd order와 상당히 다르다.  
* case2) $\alpha_r\gg\zeta\omega_n$  (5배보다 클 때) 유사한 성질을 갖는다.  
* case3) $\alpha_r=\infty$ 거의 같다. 새로운 항 금방 사라짐.  
case2, case3 로 설계하여 3rd -> 2nd approximation  

### Zero 추가  
![zero 추가](/assets/images/Control_System_img/6-11-2-zero1.jpg)  
![zero 추가](/assets/images/Control_System_img/6-11-2-zero2.jpg)  


## Time domain solution of state space equation  
![time domain solution](/assets/images/Control_System_img/6-12-time-domain-sol.jpg)  


Posting 수정 내용   
230608 포스팅 시작  
230608 포스팅 마무리  
{: .notice--success}
