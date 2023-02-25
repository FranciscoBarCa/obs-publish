---
aliases: SVM
---

#machine_learning #classification 

# How it works
## Support Vector Classifier
> [!info] Info #card
> This is not yet a SVM 

Finds an optimal [[hyperplane]] that best segregates observations from different classes. 
The optimal **hyperplane** is picked so that the **distance from its nearest points** in each space to itself is **maximized**. And these nearest points are the so-called [[support vectors]]. 
> [!danger] Very important #card
> 

![200](../assets/Pasted%20image%2020230212193620.png) ![180](../assets/Pasted%20image%2020230212194331.png)

### Optimal Hyperplane
The nearest point(s) in the positive side can constitute a hyperplane parallel to the decision [[hyperplane]], which we call a Positive [[hyperplane]]; on the other hand, the nearest point(s) in the negative side constitute the negative [[hyperplane]]. The perpendicular distance between the positive and negative hyperplanes is called the **[[SVM/Margin]]**, whose value equates to the sum of the two aforementioned distances. A Decision [[hyperplane]] is deemed optimal if the **margin is maximized.**
![](../assets/Pasted%20image%2020230207151226.png)
> [!info] Info #card > The distance from a [support vector](support%20vectors.md) to the line is the margin. 

> [!danger] Very important #card
> with No C ->⏫ Sensitivity to individual observations -> ❌Robust -> [Overfitting](Overfitting.md) 
> ![](../assets/Pasted%20image%2020230212195240.png)

### Slackness
> Normal SVM (can be solved) can exclusively be used for [[linearly separable]] problems. Unless slack terms are included or non linear terms used.
> [!warning] Importante #card Works for all type of problems
>

 We allow ignoring some points, ![](../assets/Pasted%20image%2020230207152133.png)Where **$\epsilon$** is the **cost of ignoring** a point(not a parameter) and **C** the **total slackness allowed**(parameter).
We control the slackness of the classifier by changing the value of C. 
> [!info] Info #card
> C determines the number and severity of the violations to the margin we will tolerate

> [!warning] Importante #card
> C is allso called cost 

-  **$\epsilon$ = 0**, then the observation is on the correct side of the [[margin]] 
-  **$\epsilon$ \> 0**, then the observation is on the wrong side of the [[margin]]
-  **$\epsilon$ = 1**, then the observation is on the wrong side of the [[hyperplane]]
 
  > [!info] Info #card C is obtained through [Cross Validation](Cross%20Validation.md)

 > [!danger] Very important #card
> ⏬C -> Strict and small  [Margin](../SVM/Margin.md) -> ⏬[[Bias]] ⏫ [[Variance]]
> 
> ⏫C -> Permissive and large [Margin](../SVM/Margin.md) -> ⏫[[Bias]] ⏬ [[Variance]]

# SVM
[[inner product]]
[[Kernel]]
