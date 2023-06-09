---
title: '[Control System] 05 제어공학 Similarity Transformation'
toc: true
toc_label: Table of Contents
categories:
  - Control_System
published: true
tags: [control_system]
---

# 05 제어공학 Similarity Transformation


무수히 많은 State space는 같은 Eigenvalue를 갖는다.
(Transfer function은 Unique하다)

## 1. PVCF Xp vs Controller cannical form Xc
$$ X_p =  \left[ \begin{matrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\  1 & 0 & 0 \\  \end{matrix} \right] X_c $$

## 2. Similarity transform
![similarity transform](/assets/images/Control_System_img/5-1-similarity-transform.jpg)

## 3. TF <- SS1, SS2
![TF ss1 ss2](/assets/images/Control_System_img/5-2-tf-ss1-ss2.jpg)

## 4. 같은 target의 s/s는 모두 같은 eigenvalue를 갖는다.
![same target same eigenvalue](/assets/images/Control_System_img/5-3-same-target-same-eigenvalue.jpg)

Posting 수정 내용   
230608 포스팅 시작  
230608 포스팅 마무리  
{: .notice--success}