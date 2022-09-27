---
id: cn4rsjwsl3fpw50pqmjde6f
title: Analytic Geometry
desc: ''
updated: 1664308186032
created: 1662709595196
---

## Прямая на плоскости
Прямая задаётся точкой и вектором.

(рис. 1)  
$\overrightarrow{MN} || \vec p \space \exists t \in \R : \overrightarrow {MN} = t\vec p$

$\overrightarrow{ON} = \overrightarrow{OM} + \overrightarrow{MN} = (x_0, y_0) + t(\alpha, \beta) = (x_0 + \alpha t, y_0 + \beta t)$

## Параметрическое уравнение прямой
$\begin{cases}
x = x_0 + \alpha t \\
y = y_0 + \beta t, t \in \R
\end{cases}$

### Каноническое уравнение прямой
$t = {x - x_0 \over \alpha}, t = {y - y_0 \over \beta} \iff {x - x_0 \over \alpha} = {y - y_0 \over \beta}$

(рис. 2)  
$\forall x \in l \space \overrightarrow{OX}\vec q = |\overrightarrow{OX}||\vec q|\cos \alpha = \text{const} \implies \overrightarrow{OX}\vec q = Ax + By \implies Ax + By = \text{const}$

### Общее уравнение прямой
$Ax + By + C = 0$

### Нормальное уравнение прямой
$\alpha x + \beta y - p = 0, \text{где } \alpha^2+\beta^2=1, p>0$

Общее уравнение $\to$ нормальное уравнение: $Ax + By + C = 0 \to +-({A \over \sqrt {A^2 + B^2}}x + {B \over \sqrt {A^2 + B^2}}y + {C \over \sqrt {A^2 + B^2}}) = 0$

(рис. 3)  
$\overrightarrow{OX}\vec n = \alpha x + \beta y = |\overrightarrow{OX}||\vec n| \cos \alpha = p$ - расстояние от точки $O$ до прямой $l$

(рис. 4)  
$\overrightarrow{OM}\vec n = \overrightarrow{OM}\vec n \cos \alpha = \overrightarrow{OM} \cos \alpha = OK = OL + LK = p + LK = p + \rho(M, l)$

* а) $\rho(M, l) = \alpha x_M + \beta y_M - p$
* б) $\rho(M, l) = -(\alpha x_M + \beta y_M) + p$
* в) $-(\alpha x_M+y_M)+p=\rho(M, l)$

$\rho(M, l) = |\alpha x_M + \beta y_M - p|$

### ???
(рис. 5)

### Уравнение в отрезках
(рис. 6)
${x \over a} {y \over b} = 1$

### Расстояние между параллельными прямыми
> $Ax + By + C = 0, \space Ax + By + C_1 = 0 -$ уравнения параллельных прямых

Тогда $\rho(l_1, l_2)={C_1 - C_2 \over \sqrt {A^2 + B^2}}$
