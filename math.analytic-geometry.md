---
id: cn4rsjwsl3fpw50pqmjde6f
title: Analytic Geometry
desc: ''
updated: 1664801884677
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

## Векторное произведение векторов
$\vec a, \vec b, \vec c \in \R^3\,\vec a \times \vec b = \vec c :$
* $\vec c \perp \vec a \land \vec c \perp \vec b$
* $|\vec c| = |\vec a|*|\vec b|*\sin \alpha$
* $\vec a \vec b \vec c$ - правая тройка векторов

### Свойства
1. $\vec a \times \vec a = \vec 0$
2. $\vec a \times \vec b = -\vec b \times \vec a$ - коммутативности нет
3. $\lambda \vec a \times \vec b = \lambda (\vec a \times \vec b) = \vec a \times \lambda \vec b$
4. $(!)$ $\vec c \times (\vec a + \vec b) = \vec c \times \vec a + \vec c \times \vec b$

#### Доказательство свойства 4
Лемма 1. $\vec c \times (\vec a +\lambda\vec c) = \vec c \times \vec a + \vec c \times \lambda\vec c = \vec c \times \vec a$ - (рис. 5)

Лемма 2. $\vec a \not{||} \vec c \implies \exists!\lambda : \vec c \perp \vec a + \lambda \vec c$$  
Доказательство.  
$\vec c (\vec a + \lambda \vec c) = 0 \iff \vec a \times$ *TODO*

Лемма 3. $\vec c \perp \vec a, \vec c \perp \vec a \implies \vec c \times (\vec a + \vec b) = \vec c \times \vec a + \vec c \times \vec b$  
(6)
* $|\vec c \times \vec a| = |\vec c| * |\vec a| * sin 90\degree = |\vec c| * |vec a|$
* то же самое верно для $\vec b$
* (6) $\implies \vec c \times \vec a + \vec c \times \vec b = \vec c \times (\vec a + \vec b)$

Доказательство.  
$\vec c \times (\vec a + \vec b) = \vec c \times (\vec a_1 + \lambda \vec c + \vec b_1 + \mu \vec c) = \vec c \times \vec a_1 + \vec c \times \vec b_1 = \vec c \times (\vec a + \lambda \vec c) + \vec c \times (\vec a + \lambda \vec c) + \vec c \times (\vec b + \mu \vec c) = \vec c \times \vec a + \vec c \times \vec b$

