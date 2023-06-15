---
title: '[Control System] 10 제어공학 design via root locus'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
tags: [control_system]
---

# 10 제어공학 design via root locus
![design via root locus](/assets/images/Control_System_img/10-1-design.jpg)  
제어목적  
	- stability, transient response improve -> closed loop pole  
	- steady state error improve                 -> open loop pole  

* **Improving transient response**  
![improve-transient-response](/assets/images/Control_System_img/10-2-improve-transient-response.jpg)  
  
* **Improving steady state error**  
![improve-steady-state-error](/assets/images/Control_System_img/10-3-improve-steady-state-error.jpg)  
  
* **결론**  
2 case 모두 pole, zero 추가 해야한다.  
  
## Improving steady state error via cascade
#### PI controller -> active 소자
![PI controller - active](/assets/images/Control_System_img/10-4-pi-controller.png)
  
#### Lag controller -> passive 소자  
![Lag controller - passive](/assets/images/Control_System_img/10-5-lag-controller-1.png)  
![Lag controller - passive](/assets/images/Control_System_img/10-5-lag-controller-2.png)  

## Improving transient response via cascade compensation
#### PD controller -> active 소자  
![PD controller - active](/assets/images/Control_System_img/10-6-pd-controller.png)  
  
#### Lead controller  
![Lead controller](/assets/images/Control_System_img/10-7-lead-controller.png)  
  
## Improving steady state error & transient response  
#### PID controller  
![PID controller](/assets/images/Control_System_img/10-8-pid-controller.png)  
  
#### Lag-Lead controller  
![Lag-Lead controller](/assets/images/Control_System_img/10-9-lag-lead-controller.png)  
  
## Types of cascade compensators  
![cascade compensator](/assets/images/Control_System_img/10-10-cascade-compensator.png)  


Posting 수정 내용   
230609 포스팅 시작  
230609 포스팅 마무리  
230615 줄바꿈 수정
{: .notice--success}



