---
title: '[Control System] 02 제어공학 Modeling in the Frequency Domain'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
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


## Laplace Transfrom
$$ Time(t): \mathcal{f}(t) \leftrightarrow Freq(s): \mathcal{F} (s) $$    
Laplace Transfrom  
![Laplace Transfrom](/assets/images/Control_System_img/2-2-laplace-transform.jpg)  
Inverse Laplace Transfrom   
![Inverse Laplace Transfrom](/assets/images/Control_System_img/2-3-inverse-laplace-transform.jpg)  
Laplace Transform Table  
![2-4-laplace-transform-table.jpg](/assets/images/Control_System_img/2-4-laplace-transform-table.jpg)  
Theorems  
![2-5-laplace-transform-theorems.jpg](/assets/images/Control_System_img/2-5-laplace-transform-theorems.jpg)  
  
제어공학에서 배우는 모든 target의 수학적 모델은 미분 방정식으로 표현된다. 미분 방정식은 Laplace Transform을 사용하여 간단하게 풀 수 있다.  

## The transfer function
![The transfer function](/assets/images/Control_System_img/2-6-transfer-function.jpg)

## frequency domain
* Electrical
* Mechanical
* Electrical + Mechanical

## Electrical Network Transfer Functions
* 1. Passive
![Passive](/assets/images/Control_System_img/2-7-passive.jpg)

* 2. Active
![Active](/assets/images/Control_System_img/2-9-active.jpg)

* Mesh Analysis
![Eq](/assets/images/Control_System_img/2-8-equation.jpg)

## Mechanical System Transfer Functions
* 1. Translational
![Translational](/assets/images/Control_System_img/2-10-translational.jpg)
equation  
![Eq](/assets/images/Control_System_img/2-11-translational-eq.jpg)


* 2. Rotational  
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
{: .notice--success}
