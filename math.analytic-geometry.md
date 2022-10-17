---
id: cn4rsjwsl3fpw50pqmjde6f
title: Analytic Geometry
desc: ""
updated: 1665737822010
created: 1662709595196
---

## Прямая на плоскости

Прямая задаётся точкой и вектором.

(рис. 1)  
$\overrightarrow{MN} || \vec p\ \exists t \in \R : \overrightarrow {MN} = t\vec p$

$\overrightarrow{ON} = \overrightarrow{OM} + \overrightarrow{MN} = (x_0, y_0) + t(\alpha, \beta) = (x_0 + \alpha t, y_0 + \beta t)$

## Параметрическое уравнение прямой

$\begin{cases}
x = x_0 + \alpha t \\
y = y_0 + \beta t, t \in \R
\end{cases}$

### Каноническое уравнение прямой

$t = {x - x_0 \over \alpha}, t = {y - y_0 \over \beta} \iff {x - x_0 \over \alpha} = {y - y_0 \over \beta}$

(рис. 2)  
$\forall x \in l\ \overrightarrow{OX}\vec q = |\overrightarrow{OX}||\vec q|\cos \alpha = \text{const} \implies \overrightarrow{OX}\vec q = Ax + By \implies Ax + By = \text{const}$

### Общее уравнение прямой

$Ax + By + C = 0$

### Нормальное уравнение прямой

$\alpha x + \beta y - p = 0, \text{где } \alpha^2+\beta^2=1, p>0$

Общее уравнение $\to$ нормальное уравнение: $Ax + By + C = 0 \to +-({A \over \sqrt {A^2 + B^2}}x + {B \over \sqrt {A^2 + B^2}}y + {C \over \sqrt {A^2 + B^2}}) = 0$

(рис. 3)  
$\overrightarrow{OX}\vec n = \alpha x + \beta y = |\overrightarrow{OX}||\vec n| \cos \alpha = p$ - расстояние от точки $O$ до прямой $l$

(рис. 4)  
$\overrightarrow{OM}\vec n = \overrightarrow{OM}\vec n \cos \alpha = \overrightarrow{OM} \cos \alpha = OK = OL + LK = p + LK = p + \rho(M, l)$

- а) $\rho(M, l) = \alpha x_M + \beta y_M - p$
- б) $\rho(M, l) = -(\alpha x_M + \beta y_M) + p$
- в) $-(\alpha x_M+y_M)+p=\rho(M, l)$

$\rho(M, l) = |\alpha x_M + \beta y_M - p|$

### ???

(рис. 5)

### Уравнение в отрезках

(рис. 6)
${x \over a} {y \over b} = 1$

### Расстояние между параллельными прямыми

> $Ax + By + C = 0,\ Ax + By + C_1 = 0 -$ уравнения параллельных прямых

Тогда $\rho(l_1, l_2)={C_1 - C_2 \over \sqrt {A^2 + B^2}}$

## Векторное произведение векторов

$\vec a, \vec b, \vec c \in \R^3\,\vec a \times \vec b = \vec c :$

- $\vec c \perp \vec a \land \vec c \perp \vec b$
- $|\vec c| = |\vec a|*|\vec b|*\sin \alpha$
- $\vec a \vec b \vec c$ - правая тройка векторов

### Свойства

1. $\vec a \times \vec a = \vec 0$
2. $\vec a \times \vec b = -\vec b \times \vec a$ - коммутативности нет
3. $\lambda \vec a \times \vec b = \lambda (\vec a \times \vec b) = \vec a \times \lambda \vec b$
4. $(!)$ $\vec c \times (\vec a + \vec b) = \vec c \times \vec a + \vec c \times \vec b$

#### Доказательство свойства 4

Лемма 1. $\vec c \times (\vec a +\lambda\vec c) = \vec c \times \vec a + \vec c \times \lambda\vec c = \vec c \times \vec a$ - (рис. 5)

Лемма 2. $\vec a \not{||} \vec c \implies \exists!\lambda : \vec c \perp \vec a + \lambda \vec c$$  
Доказательство.  
$\vec c (\vec a + \lambda \vec c) = 0 \iff \vec a \times$ _TODO_

Лемма 3. $\vec c \perp \vec a, \vec c \perp \vec a \implies \vec c \times (\vec a + \vec b) = \vec c \times \vec a + \vec c \times \vec b$  
(6)

- $|\vec c \times \vec a| = |\vec c| *|\vec a|* sin 90\degree = |\vec c| * |vec a|$
- то же самое верно для $\vec b$
- (6) $\implies \vec c \times \vec a + \vec c \times \vec b = \vec c \times (\vec a + \vec b)$

Доказательство.  
$\vec c \times (\vec a + \vec b) = \vec c \times (\vec a_1 + \lambda \vec c + \vec b_1 + \mu \vec c) = \vec c \times \vec a_1 + \vec c \times \vec b_1 = \vec c \times (\vec a + \lambda \vec c) + \vec c \times (\vec a + \lambda \vec c) + \vec c \times (\vec b + \mu \vec c) = \vec c \times \vec a + \vec c \times \vec b$

## Смешанное произведение векторов

$\vec a \vec b \vec c = \vec a \times \vec b \vec c$

$$
\vec a = (a_x, a_y, a_z) \\
\vec b = (b_x, b_y, b_z) \\
\vec c = (c_x, c_y, c_z) \\
$$

$$
\vec a \vec b \vec c = \begin{vmatrix}
a_x & a_y & a_z \\
b_x & b_y & b_z \\
c_x & c_y & c_z
\end{vmatrix}$$

### Геометрический смысл

(рис. 1)  
$\vec a \vec b \vec c = S_\text{параллелограмм} |\vec a| \cos \alpha =$ объём параллелепипеда, натянутого на $\vec a, \vec b, \vec c$ с точностью до знака._Тот же, что и геометрический смысл определителя матрицы_

### Свойства

- _TODO, переписать из тетради_

## Уравнение плоскости

$A(x_1, y_1, z_1), B(x_2, y_2, z_2), C(x_3, y_3, z_y), X(x, y, z); A, B, C \in \pi$  
$$X \in \pi \iff \overrightarrow{AX}\overrightarrow{AB}\overrightarrow{AC}=0 \iff
\begin{vmatrix}
x-x_1 & y-y_1 & z-z_1 \\
x-x_2 & y-y_2 & z-z_2 \\
x-x_3 & y-y_3 & z-z_3
\end{vmatrix} = 0$$

(рис. 2)  
$\vec n = (\alpha, \beta, \gamma); X(x, y, z)$  
$\alpha x + \beta y + \gamma z - p = 0$ - нормальное уравнение плоскости

(рис. 3)  
$M(x, y, z)$  
$\overrightarrow{OM} = (x, y, z)$  
$\overrightarrow{OM} \vec n = \alpha x + \beta y + \gamma z = |\overrightarrow{OM}||\vec n| \cos \gamma = |\overrightarrow{OM}| \cos \gamma = \overrightarrow{ON} = p + \rho(M, \pi)$  
$\implies \rho(M, \pi) = |\alpha x + \beta y + \gamma z - p|$

Расстояние от точки $M(x, y, z)$ до плоскости $\pi$ получается подстановкой $x, y, z$ в нормальное уравнение плоскости

### Расстояние между плоскостями

_ноут садится_

## Прямая в пространстве

$$\begin{cases}
A_1x + B_1y + C_1z + D_1 = 0 \\
A_2x + B_2y + C_2z + D_2 = 0
\end{cases},\vec n_1 \times \vec n_2 \neq 0$$

(рис. 4)  
$$N \in l \iff \overrightarrow{MN} || \vec p \iff \exists t : t\overrightarrow{MN} = \vec p \iff \begin{cases}
x = x_0 + t\alpha \\
y = y_0 + t\beta \\
z = z_0 + t\gamma
\end{cases}, t \in \R - \text{параметрическое уравнение прямой}$$

При $t={x-x_0 \over \alpha}={y-y_0 \over \beta}={z-z_0 \over \gamma}$ - каноническое уравнение прямой

## Пересечение прямой и плоскости
Пусть $l : {x+2 \over 3} = {y - 1 \over 2} = {z - 3 \over 1}, \pi : x + 5y - 2z -3 = 0$  
$\vec p \not\perp\vec n \implies l \cap \pi \neq \emptyset$

$$
(-2+3t)+5(1+2t)-2(3-t)-3= 0 \iff 15t-6 = 0 \iff t = 0,4 \\
\implies
\begin{matrix}
x =& -2+3*0,4 &= -0,8 \\
y =& 1 + 2*0,4 &= 1,8 \\
z =& 3 - 0,4 &= 2,6
\end{matrix}
$$

## Взаимное расположение прямых
* прямые совпадают
* прямые параллельны
* прямые пересекаются
* прямые скрещиваются $\iff \overrightarrow{M_1M_2}\vec p_1 \vec p_2 \neq 0$  
  $\exists! l_3 : l_3 \perp l_1, l_3 \perp l_2$
### Расстояние между параллельными прямыми
$$l_1 : \begin{cases}
x = 2 + t \\
y = -3-2t \\
z = 3t
\end{cases}\quad
l_2 : \begin{cases}
x = -2t \\
y = 1 + 4t \\
z = 5 - 6t 
\end{cases}$$

Пусть $M_0(2; -3; 0) \in l_1, M_0 \notin l_2; M_1(0; 1; 5) \in l_2$  
(рис. 1)  
$\rho(l_1, l_2) = h = {S_{пр} \over |\vec p_1|} = {|\vec p_1 \times \overrightarrow{M_1M_0}| \over |\vec p_1|}$

### Точка пересечения
$\vec n = \vec p_1 \times \vec p_2 \implies \pi \supset l_2, \pi || l_1$  

*задача: найти точку пересечения двух прямых в пространстве*

### Расстояние между скрещивающимися прямыми

(рис. 2) 
$$
\exists \pi_1 \supset l_1, \pi_2 \supset l_2 : \pi_1 \perp l_2, \pi_2 \perp l_2 \\
\rho(l_1, l_2) = \rho(\pi_1, \pi_2) = h_{пар.}={V_{p_1, p_2, \overrightarrow{M_1M_2}} \over S_{p_1 \times p_2}}
$$

## Поверхности второго порядка

Поверхность второго порядка в $\R^3$ - множество точек в $R^3$, координаты которых удовлетворяют уравнению: 
$$
ax^2 + bxy + cy^2 + dz^2 + exz + fyz + kx + ly + mz + n = 0
$$

Любое сечение поверхности второго порядка плоскостью - кривая второго порядка (на примере эллипсоида):
$$
Ax + By + Cz + D = 0 \\
{x^2 \over a^2} + {y^2 \over b^2} + {({D-Ax-By \over C})^2 \over c^2} = 1
$$

### Канонические поверхности

* ${x^2 \over a^2} + {y^2 \over b^2} + {z^2 \over c^2} = 1$ - эллипсоид; его сечение координатными плоскостями - эллипсы. (рис. 3)
* ${x^2 \over a^2} + {y^2 \over b^2} - {z^2 \over c^2} = 0$ - конус второго порядка (рис. 4)