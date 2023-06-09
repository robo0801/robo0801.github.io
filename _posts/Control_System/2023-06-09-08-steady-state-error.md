---
title: '[Control System] 08 제어공학 Steady State Error'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
tags: [control_system]
---

# 08 제어공학 Steady State Error

## Define
$\lim_{t\rightarrow\infty} \text{output-input}=e(\infty)$

input
	- step: $r(t)=u(t)$ $\rightarrow$ ${1\over s}$
	- ramp: $r(t)=tu(t)$ $\rightarrow$ ${1\over s^2}$
	- parabolic: $r(t)={1\over 2}t^2 u(t)$ $\rightarrow$ ${1\over s^3}$
![define](/assets/images/Control_System_img/8-1-define.jpg)

## for unity feedback system
(feedback gain = 1)
![for unity feedback system](/assets/images/Control_System_img/8-2-unity-feedback-system.jpg)
$$
C(s)={G(s) \over {1+G(s)H(s)}} R(s) = G(s)E_a(s)
$$
$$
\rightarrow E_a(s)={R(s) \over {1+G(s)H(s)}}=R(s)-H(s)C(s)
$$
Unity system
$$E(s)={R(s) \over{1+G(s)}}=R(s)-C(s)$$
Steady State Error
$$e_ss=\lim_{t\rightarrow \infty} e(t)=\lim_{s \rightarrow 0}{sR \over {1+G}}$$

### constants & system type
![constants](/assets/images/Control_System_img/8-3-constants.jpg)

system type
![system type](/assets/images/Control_System_img/8-4-system-type.jpg)

### pole과 spec
transient response: closed loop 의 pole
stability                 : closed loop 의 pole
steady state error : open loop 의 pole (feedback 계산 전, 원점에 몇 개)


## for nonunity feedback
![for nonunity feedback system](/assets/images/Control_System_img/8-5-non-unity-feedback.jpg)


Posting 수정 내용   
230609 포스팅 시작  
230609 포스팅 마무리  
{: .notice--success}