---
id: 2hIQXnXNTHYOFGbFQ3xP1
title: Integral
desc: ''
updated: 1663267348756
created: 1631627730961
---
_2021-09-14: первая попытка перенести материалы по школьным предметам в базу_


 ## Первообразная (аntiderivative)
 > Функция $F(x)$ называется первообразной функции $f(x)$ на промежутке $A$, если $\forall x \in A: F'(x) = f(x)$

 Например, $F(x) = sin(x)$ - первообразная функции $f(x) = \cos x$, т.к. $(\frac {x^4} 4)' = x^3$

 ### Правила нахождения

 | Функция | Первообразная |
 | ------- | ------------- |
 | $x^p, p \not= -1$ | $\frac {x^{p+1}} {p+1}+C$
 | $\frac 1 x, x>0$ | $\ln x+C$
 | $e^x$ | $e^x+C$
 | $\sin x$ | $-\cos x+C$
 | $\cos x$ | $\sin x+C$
 | $(kx+b)^p, p \not=-1, k \not=0$ | $\frac {(kx + b)^{p+1}} {k(p+1)} + C$
 | $\frac 1 {kx+b}, k \not=0$ | $\frac 1 k \ln (kx+b)+C$
 | $\sin (kx+b), k \not=0$ | $-\frac 1 k \cos (kx+b)+C$
 | $\cos (kx+b), k \not=0$ | $\frac 1 k \sin (kx+b)+C$

 > Пусть $F(x)$ и $G(x)$ - первообразные функций $f(x)$ и $g(x)$ на некотором промежутке. Тогда:  
 1. $(F(x)\pm G(x))' = f(x)\pm g(x)$
 2. $(aF(x))' =af(x)$

## Интеграл
Упрощая, интеграл - это площадь под кривой, заданной функцией $f(x)$, на отрезке $[a; b]$

Строго говоря, интеграл - это предел суммы прямоугольников $x_i * f(x_{i+1}-x_i)$ при $i \rarr \infty$

> $\displaystyle\int _a ^b f(x)dx = F(b) - F(a) = S$

Простой случай, когда для функции можно найти первообразную

## Свойства

$\displaystyle\int _0 ^\infty e^{-x}dx=1$

$\displaystyle\int _a ^b f(\alpha x)dx = 1/\alpha \displaystyle\int _{\alpha a} ^{\alpha b} f(\alpha x)\alpha dx=1/\alpha \displaystyle\int _{\alpha a} ^{\alpha b} f(x)dx$ 

$\frac {dx}x=\alpha dt\implies x=Ce^{\alpha t}$, где $C$ - константа
