---
title: '[Control System] 02 제어공학 Modeling in the Frequency Domain'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
use_math: true
tags: [control_system]
---
# 02 제어공학 Modeling in the Frequency Domain

## 제어기 설계(Controller Design)
![Model](/assets/images/Control_System_img/2-1-target-modeling.jpg)

Specification  
- transient response  
- steady state error  
- stability  


제어할 모델(plant)과 완전히 같은 수학적 modeling  
Modeling은 Laplace Transform을 사용하여 Frequency Domain과 Time Domain으로 변환한다.  
(학부에서는 선형 방정식만 다루고, 대학원에서 비선형 방정식을 다룬다.) 

## Laplace Transfrom  
Plant의 미분 방정식을 대수 방정식으로 바꾸어 쉽게 해석하고 설계 가능  
$$Time(t):\mathcal{f}(t)\leftrightarrow Freq(s):\mathcal{F}(s)$$      
* Laplace Transfrom  
$$
F(s)=\mathcal{L}\{f(t)\}
=\int_{0^-}^{\infty} f(t)e^{-st}\,dt
$$  
![Laplace Transfrom](/assets/images/Control_System_img/2-2-laplace-transform.jpg)  
* Inverse Laplace Transfrom  
$$
\begin{aligned}
f(t)u(t)
&=\mathcal{L}^{-1}\{F(s)\}
=\frac{1}{2\pi j}
\int_{\sigma-j\infty}^{\sigma+j\infty}
F(s)e^{st}\,ds,\\
u(t)
&=
\begin{cases}
0, & t<0,\\
1, & t\ge0.
\end{cases}
\end{aligned}
$$  
![Inverse Laplace Transfrom](/assets/images/Control_System_img/2-3-inverse-laplace-transform.jpg)  
* Unit Step Function  
$$
u(t)=
\begin{cases}
0, & t<0,\\
1, & t\ge0.
\end{cases}
$$  

* Laplace Transform Table  
![2-4-laplace-transform-table.jpg](/assets/images/Control_System_img/2-4-laplace-transform-table.jpg)  
* Theorems  
![2-5-laplace-transform-theorems.jpg](/assets/images/Control_System_img/2-5-laplace-transform-theorems.jpg)  
  
제어공학에서 배우는 모든 target의 수학적 모델은 미분 방정식으로 표현된다. 미분 방정식은 Laplace Transform을 사용하여 간단하게 풀 수 있다.  

## The transfer function
전달 함수(Transfer function): Input이 Output에 어떤 영향을 주는지 나타내는 시스템의 수학적 모델  
![The transfer function](/assets/images/Control_System_img/2-6-transfer-function.jpg)
* 전달함수의 한계 
  선형(Linear) 시스템만 적용 가능: 입력과 출력이 비례 
  시간 불변(Time-Invariant, LTI) 시스템만 적용 가능: 시스템 특성이 시간에 따라 변하지 않는다. 
  시스템 내부 상태 알 수 없다.  
  초기 조건을 포함하지 않는다.: 초기 조건이 모두 0이라 가정  
## frequency domain
* Electrical  
* Mechanical  
* Electrical + Mechanical  

## Electrical Network Transfer Functions
* 1.Passive  
![Passive](/assets/images/Control_System_img/2-7-passive.jpg)

* 2.Active  
![Active](/assets/images/Control_System_img/2-9-active.jpg)
Ideal Op-Amp(이상적인 Op-Amp)의 두 가지 성질(가정)
1.입력 전류가 0
$$i_{+}=i_{-}=0$$  
2. 음에 피드백에 걸려있으면 두 입력 전압이 같다.
$$V_{+}=V_{-}$$  

* Mesh Analysis  
![Eq](/assets/images/Control_System_img/2-8-equation.jpg)

## Mechanical System Transfer Functions
* 1.Translational  
![Translational](/assets/images/Control_System_img/2-10-translational.jpg)
equation  
![Eq](/assets/images/Control_System_img/2-11-translational-eq.jpg)

* 2.Rotational  
![Rotational](/assets/images/Control_System_img/2-12-rotational.jpg)  
equation  
![Eq](/assets/images/Control_System_img/2-13-rotational-eq.jpg)  
Gear  
![Gear](/assets/images/Control_System_img/2-14-gear.jpg)  


## Electromechanical System
예시: DC Motor  
![2-15-dc-motor.jpg](/assets/images/Control_System_img/2-15-dc-motor.jpg)


Posting 수정 내용   
220105 포스팅 시작  
230606 포스팅 추가 (마지막까지)  
260718 수식 수정  
260719 전달함수 설명 추가, opamp 조건 추가  
{: .notice--success}
