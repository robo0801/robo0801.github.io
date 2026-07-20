---
title: '[Control System] 04 제어공학 Converting State Space to Transfer Function'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
use_math: true
tags: [control_system]
---
# 04 제어공학 Converting State Space to Transfer Function
여러 해가 있는 state space를 구해서 유일한 transfer function을 구한다.  
PVCF, Cascade, Parallel, CCF, OCF 5가지 중 PVCF를 제외한 4가지는 signal flow graph를 이용하여 구하는 방법이다.  
## 1. PVCF (phase variable canonical form)
출력과 출력의 미분을 상태변수로 정의하는 방법  
$$ 
x_{1}=y, x_{2}=\dot{y}, x_{3}=\ddot{y}
$$  
특징: Companion Matrix 형태이고 직관적, 미분방정식에서 쉽게 유도 가능  
![PVCF](/assets/images/Control_System_img/4-1-PVCF.jpg)

## 2. Cascade  
전달함수를 1차 or 2차 시스템들의 직렬연결(Cascade)로 분해한 뒤 state space로 표현하는 방법    
![cascade](/assets/images/Control_System_img/4-2-cascade.jpg)

## 3. Parallel
* 전달함수를 부분분수 전개(Partial Fraction Expansion) 한 뒤 병렬 연결로 표현  
* 특징: 부분분수 전개 필요, 극점(Pole)이 명확히 보임, 응답 해석이 쉬움  
![Parallel](/assets/images/Control_System_img/4-3-parallel.jpg)

## 4. Controller Canonical Form
* 제어가능성(Controllability)을 분석하기 쉽도록 만든 표준형  
* 특징:  
  PVCF의 Matrix 위 아래 뒤집힌 형태  
  입력이 마지막 상태에 들어감  
  Contrallability Matrix 계산이 쉬움  
  State Feedback 설계에 많이 사용  
![Controller Canonical Form](/assets/images/Control_System_img/4-4-ccf.jpg)

## 5. Observer Canonical Form
* 관측가능성(Observability)을 분석하기 쉽게 만든 표준형  
* 특징:  
  분모 문자를 최고 차수로 나눈 뒤 계산  
  CCF를 전치(Transpose)한 형태와 비슷  
  Observer 설계에 많이 사용  
  Observability Matrix 계산이 쉬움  

![Observer Canonical Form](/assets/images/Control_System_img/4-5-ocf.jpg)

## Controller와 Observer 관계
![4-6-controller-observer.png](/assets/images/Control_System_img/4-6-controller-observer.png)

## Controllability Matrix, Observability Matrix   
Controllability Matrix, Observability Matrix 계산이 쉽다.  
이유는 아래에  
### Controllability Matrix 계산이 쉬운 이유  
* state space 행렬  
$$
A=
\begin{matrix}
0 & 1 & 0 & \cdots & 0 \\
0 & 0 & 1 & \cdots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
-a_0 & -a_1 & -a_2 & \cdots & -a_{n-1}
\end{matrix}

B=
\begin{matrix}
0 \\
0 \\
\vdots \\
1
\end{matrix}
$$  

* Controllability Matrix  
$$
\mathcal{C}
=
\begin{bmatrix}
B & AB & A^2B & \cdots & A^{n-1}B
\end{bmatrix}
$$  

* 계산 과정  
  * step 1. $$B$$  
    $$
    B=
    \begin{bmatrix}
    0 \\
    0 \\
    1
    \end{bmatrix}
    
    $$  
  * step 2. $$AB$$  
    $$
    AB
    =
    A
    \begin{bmatrix}
    0 \\
    0 \\
    1
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 \\
    1 \\
    -a_2
    \end{bmatrix}
    $$  
  * step 3. $A^{2}B$  
    $$
    B
    \;\rightarrow\;
    AB
    \;\rightarrow\;
    A^2B
    \;\rightarrow\;
    A^3B 
    $$  
  같은 행렬 $$A$$를 반복해서 곱하면 되므로 계산이 규칙적이고 간단하다.


### Observability Matrix 계산이 쉬운 이유
출력이 첫 번째 상태를 직접 측정하도록 C행렬이 구성되어 있음

* State space matrix
$$
C=
\begin{bmatrix}
1 & 0 & 0
\end{bmatrix}
$$  
* Observability matrix
$$
\mathcal{O}
=
\begin{bmatrix}
C \\
CA \\
CA^2 \\
\vdots \\
CA^{n-1}
\end{bmatrix}
$$  
* 계산 과정
  * Step 1. $$C$$  
    $$
    C=
    \begin{bmatrix}
    1 & 0 & 0
    \end{bmatrix}
    $$  
  * Step 1. $$CA$$  
    $$
    CA=
    \begin{bmatrix}
    -a_2 & 1 & 0
    \end{bmatrix}
    $$  
  * step 3. $$CA^{2}$$  
    $$
    C
    \;\rightarrow\;
    CA
    \;\rightarrow\;
    CA^2
    \;\rightarrow\;
    CA^3 
    $$  
  같은 행렬 $$A$$를 반복해서 곱하면 되므로 계산이 규칙적이고 간단하다.  
  출력으로 상태를 차례로 알아낼 수 있다.  


Posting 수정 내용   
230607 포스팅 시작  
230607 포스팅 마무리  
230608 controller 와 observer 관계 추가  
260720 각 변환 설명과 특징 추가  
260720 CCF, OCF Matrix 계산 쉬운 이유 추가  
{: .notice--success}