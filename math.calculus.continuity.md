---
id: pghodn1csckxp4cn7frwu3o
title: Непрерывность
desc: ""
updated: 1664962579097
created: 1664803523333
---

## Непрерывность

> Определенение.  
> $f(x)$ непрерывна в $x_0 \iff \exists \lim\limits_{x \to x_0}=f(x_0)$  
> $f(x)$ непрерывна в $x_0 \iff \exists \lim\limits_{\Delta x \to 0}\Delta f(x_0) = 0$  
> $f(x)$ непрерывна слева (справа) в $x_0 \iff \exists \lim\limits_{x \to x_0-0 (+0)}=f(x_0)$

"график непрерывной функции можно нарисовать, не отрывая руки"

### Пример разрывной функции

- $f(x) = [x]$ - разрывна слева в целых точках

> $f(x)$ непрерывна на $M \iff \forall x_0 \in M \implies f(x)$ непрерывна в $x_0$

### Примеры непрерывных функций

- $f(x)=C$
- $f(x)=x$
- $f(x)=a_nx^n+a_{n-1}x^{n-1}+..+a_0\,\forall a_i \in \R$
- $f(x)={P_m \over Q_n} : Q_n(x) \neq 0$
- $f(x)=\sin x$

### Разрывы

> Определение.  
> Точка $x_0$ называется точной разрыва первого рода, $\iff f(x)$ не непрерывна в $x_0$ и:
>
> - $\exists \lim\limits_{x \to x_0 - 0} f(x) = A$
> - $\exists \lim\limits_{x \to x_0 + 0}f(x) = B$
> - $A, B \in \R$
>
> $A=B \implies x_0 -$ точка устранимого разрыва

#### Пример

- ${x^2-3x+2 \over x-1}, x \neq 1 \implies f(x)=x-2, x \neq 1; x=1 -$ точка устранимого разрыва
- $y = {sin x \over x}, x -$ точка устранимого разрыва

#### Разрыв второго рода

> $x_0$ называется точкой разрыва второго рода $\iff x_0 -$ точка разрыва, которая не является разрывом первого рода

##### Примеры

- $y = {1 \over x}, x = 0 -$ разрыв второго рода (пределы равны +$\infty$ и -$\infty$)
- $y = e^{1 \over x} x = 0 -$ разрыв второго рода (левый предел существует и равен нулю, правый предел не существует)
- $y = sin {1 \over x} -$ пределов не существует

### ???

- $\lbrace x_n \rbrace \subset [0, 1] \implies lim x_n \in [0, 1]$
- $\lbrace x_n \rbrace \subset (0, 1) \implies lim x_n \in [0, 1]$

### Функция непрерывна на отрезке

$f(x)$ непрерывна на $[a, b] \implies f(x)$ ограничена на $[a, b]$
Доказательство. От противного: пусть $f(x)$ не опраничена $\iff \forall n \in \N \exists x_n \in [a, b] : |f(x_n)| > n \implies \exists \lbrace x_n \rbrace$ - последовательность, которая ограничена и по теореме Больцано-Вейерштрасса $\exists \lbrace x_{n_k} \rbrace \subset \lbrace x_n \rbrace : \exists \lim\limits_{k \to \infty} x_{n_k} = c, c \in [a, b] \implies \lim\limits{k \to \infty} f(x_{n_k})=f(c)=A \iff$ противоречие, т.к. $|f(x_{n_k})| >n_k \to \infty$ при $k \to \infty$

#### Теорема Вейерштрасса

Пусть $f(x)$ непрерывна на $[a, b]$. Тогда $\exists c_1, c_2 \in [a, b] : f(c_1) = \displaystyle\max_{x \in [a, b]} f(x), f(c_2) = \displaystyle\min_{x \in a, b} f(x)$

Доказательство.  
$f(x)$ - ограниченная $\implies \exists M>0 : |f(x)| < M \implies \lbrace f(x) \rbrace$ имеет [[точную верхнюю грань |math.calculus.inf-sup]] - $\exists \displaystyle\sup_{x \in [a, b]} f(x)=A \implies$ имеем $\lbrace x_n \rbrace \implies$ (Б.В.) $\exists \lbrace x_{n_k} \subset \lbrace x_n \rbrace : \lim\limits_{k \to \infty} x_{n_k}=c,$ где $c \in [a, b] \implies f(x)$ непрерывна в т.с. $\implies$

Т3. Пусть $f(x)$ непрерывна на $[a, b]$, причём $f(a)*f(b) < 0$, тогда $\exists c \in [a, b] : f(c) = 0$

Доказательство.

- делим отрезок $[a, b]$ пополам, берём точку c*1... имеем систему вложенных отрезков $\\lbrace I_n \\rbrace : \\lim\\limits*{n \\to \\infty} |I*n| = 0, f(a_n)&lt; 0, f(b_n)>0 \\implies \\exists!c=\\displaystyle\\bigcap^\\infty*{n=1} I_n, c \\in [a, b] &#x3A; f(c) = 0$  
  Замечание: $f(a_n) < 0, f(b_n) > 0 -$ всегда  
  $\dots \lim f(a_n) = \lim f(b_n) = f(c) = 0!$

Т4. Пусть $f(x)$ непрерывна на $[a, b]$. $A = \displaystyle\max_{x \in [a, b]} f(x), B = \displaystyle\min_{x \in a, b} f(x)$, тогда $\forall C \in [B, A] \implies \exists c \in [a, b] : f(c) = C$

(BДоказательство. Пусть $f(a) = A, f(b) = B$. Пусть $F(x)=f(x)-C -$ непрерывна на $[a, b], F(a) = f(a)-C=A-C > 0, F(b)=B-C<0 \implies F(a)*F(b)<0$ и по теореме (Вейерштрасса?) $\exists c \in [a, b] : F(c) = 0 \iff f(c) = C$
