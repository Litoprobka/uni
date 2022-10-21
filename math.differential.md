---
id: 1l6c097z8c1sn5mvqly2g9d
title: Differential
desc: ''
updated: 1666360272457
created: 1666332725007
---

$$\Delta f(x, \Delta x) = f(x + \Delta x) - f(x) = f'(x)\Delta x + \epsilon(\Delta x), \text{ где } \epsilon(\Delta x) = {\Delta f(x, \Delta x) \over \Delta x}, {\epsilon(\Delta x) \to 0 \atop \Delta x \to 0}
$$

(картинка с касательной, которую мне лень рисовать)

> Главная линейная часть прирощения функции в $\Delta f(x)$ называется дифференциалом функции: $df(x) = f'(x)\Delta x$

$$
df(x) = f'(x)dx
$$

Приращение функции $f(x) = df(x) + o(\Delta x)$

## Примеры

* $f(x) = x \implies df(x) = f'(x)\Delta x = (x)'\Delta x = \Delta x$  
  $dx = \Delta x$  
  $\implies df(x) = f'(x)dx$

## Дифференцируемость

Пусть $\exists f'(x) \implies \Delta f(x)\Delta x + o(\Delta x)$

Функция $f(x)$ называется дифференцируемой в $x$, если $\exists A \in \R : \Delta f(x) = A\Delta x + o(\Delta x)$ в некоторой окрестности $U(x)$

### Связь с производной

Теорема. $f(x)$ имеет производную в $x_0 \iff f(x)$ дифференцируема в $x_0$

#### Доказательство

Пусть $\Delta f(x) = A\Delta x + o(\Delta x)$ в $U(x)$  
$\lim\limits_{\Delta x \to 0} {A\Delta x + o(\Delta x) \over \Delta x} = \lim\limits{} (A + {o(\Delta x \to 0) \over \Delta x}) = A \implies \exists f'(x_0) = A$

$$
f'(x) = {df(x) \over dx} \\
\Delta f(x, \Delta x) \approx df(x)
$$

#### Пример

* вычислить приближённо $^4\sqrt{623}$  
  возьмём $x_0 = 625, \Delta x = -2 \implies f(623) \approx f(625) + f'(625)(-2)$  
  $f(x_0) = 5 \\
  f'(x) = {x^{-3/4} \over 4} \\
  f(623) = 5-2{625^{-3/4} \over 4} = 5-2{1 \over 500} = 4,996$

## Дифференциалы высших порядков

### Свойства дифференциала первого порядка

* $dC = 0$
* $dAf(x) = Adf(x)$
* $d(f(x) + g(x)) = df(x) + dg(x)$
* $d(f(x)g(x)) = f(x)dg(x) + g(x)df(x)$
* $d{f(x) \over g(x)} = {g(x)df(x) - f(x)dg(x) \over g^2(x)}$

Свойства доказываются через аналогичные свойства производной

## Дифференциал второго порядка

> $$
d^2f(x) = d(df(x)) = d(f'(x)dx) = df'(x)dx + f'(x)d(dx) = f''(x)dxdx + 0 = f''(x)dx^2$$
>
> $$
d^nf(x) = d(d^{n-1}f(x)) \text{ тогда, если $x$ - независимая переменная, то } d^nf(x) = f^{(n)}(dx)^n
> $$

### Инвариантность первого дифференциала

Пусть $x = x(t)$, где $t$ - независимая переменная $\implies f(x) = f(x(t)) \implies df(x(t)) = (f(x(t)))'_tdt = f'_x(x(t))x'(t)dt = f'_x(x(t))d(x(t))$

### Второй дифференциал не инвариантен

$d^2(f(x(t))) = d(f'(x(t)) dx(t)) = df'(x(t))dx(t) + f'(x(t))d(dx(t)) = f''_x(x(t))dx(t)dx(t) + f'_x(x(t))d^2x(t) = f''_x(x(t))(dx(t))^2 + f'_x(x(t))x''(t)(dt)^2$
