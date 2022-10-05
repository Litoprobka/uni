---
id: ar9abllhc7rlg1rgm3r1wqe
title: Предел последовательности
desc: ""
updated: 1664958747559
created: 1663265851396
---

## Определение последовательности

[[Отображение|math.function]] $f : \N \to X$ называется последовательностью элементов множества $X$  
В контексте лекций по матану речь обычно идёт о последовательностях действительных чисел, то есть $f : \N \to \R$.

### Пример последовательности

$a_n = {(-1)^n \over n} \quad a_1 = -1, a_2 = 1/2, a_3 = 1/3 \dots$

> Множество называется счётным, если все его элементы можно записать в виде последовательности.

## Определение предела

> Число $a \in R$ называется пределом последовательности $\lbrace x_n \rbrace$, если $\forall \epsilon >0 \exists N_\epsilon \in \N : \forall n > N_\epsilon \implies |x_n - a| < \epsilon$ и записывается $\lim\limits_{n \to \infty} x_n = a$

$U_\epsilon(a) = \lbrace x : |x - a| < \epsilon \rbrace$ - $\epsilon$-окружность

> Число $а=\lim\limits_{n \to \infty} x_n$, если $\forall \epsilon > 0$ вне окрестности $U_\epsilon(a)$ содержится конечное число членов последовательности $\lbrace x_n \rbrace$

## Примеры

- $\lim\limits_{n \to \infty} {1 \over n}=0$  
  $|{1 \over n} - 0| < \epsilon \implies n > {1 \over \epsilon} \implies N_\epsilon=[{1 \over \epsilon}]$
- $\lbrace q^n \rbrace, 0<q<1 \\  
  \lim\limits_{n \to \infty} q^n = 0 \\
  |q^n-0|<\epsilon \implies q^n < \epsilon \implies 
  n \ln q < \ln \epsilon \implies n > {\ln \epsilon \over \ln q}, N_\epsilon=[{\ln \epsilon \over \ln q}]$

> $X_n$ - ограниченная, если $\exists M>0 : \forall n \in \N \ \ |X_n| \leq M$

## Свойства пределов последовательности

1. > $\exists \lim\limits_{n \to \infty} x_n=a \implies \exists! \lim\limits_{n \to \infty} x_n=a$

   Доказательство: пусть $b=\lim\limits_{n \to \infty} x_n, b \neq a \\
   \epsilon \in \R: U_\epsilon(b) \cap U_\epsilon(b) = \emptyset \implies$ противоречие

2. > $\exists \lim\limits_{n \to \infty} x_n=a, a \in \R,$ то $\lbrace x_n \rbrace$ - ограниченная

   Доказательство: для $\epsilon = 1\,\exists N_1 \in \N : \forall n>N_1 \implies |x_n-a| < 1 \implies x-1 \leq x_n \leq x + 1$, тогда $M = max \lbrace |x_1|, |x_2|...|x_n|, |a-1|, |a +1| \rbrace$

3. > $\exists \lbrace x_n \rbrace, \lbrace y_n \rbrace : x_n \leq y_n \forall n \in \N \implies \text{если } \exists \lim\limits_{n \to \infty} x_n=a, \lim\limits_{n \to \infty} y_n=b,$ то $a \leq b$

   Доказательство: _TODO_

4. > $\exists \lim\limits_{n \to \infty} x_n=a, a\neq 0 \implies \exists N_0 \in \N : (\forall n>N_0\ \implies |x_n| > {|a| \over 2})$

   Доказательство:  
   Пусть $\epsilon = a/2 \implies \exists N_0 \in \N : \forall n \in \N : n > N_0 \implies |x_n - a| < {|a| \over 2} \iff -{|a| \over 2} < x_n -a<{|a| \over 2} \implies a - {|a| \over 2} < x_n < a + {|a| \over 2}$

   Если $a > 0$: ${a \over 2} < x_n < {3a \over 2}$  
   Если $a < 0$: $x_n < {a \over 2} \implies |x_n| > {|a| \over 2}$

5. > $x_n<y_n<z_n, \exists \lim\limits_{n \to \infty} x_n = \lim\limits_{n \to \infty} z_n = a \implies \exists \lim\limits_{n \to \infty} y_n = a$.

   Доказательство: _TODO_

### Арифметические действия с предельными последовательностями

> Теорема 6. Пусть $a=\lim\limits_{n \to \infty} x_n, b=\lim\limits_{n \to \infty} y_n, a, b \in \R$  
> Tогда:
>
> 1. $\exists \lim\limits_{n \to \infty} Ax_n = Aa, \forall A\in\R$
> 2. $\exists \lim\limits_{n \to \infty} (x_n+y_n) = a + b$
> 3. $\exists \lim\limits_{n \to \infty} (x_n*y_n) = a * b$
> 4. $b \neq 0 \implies \exists \lim\limits_{n \to \infty} (x_n/y_n) = a / b$

#### Доказательства

1. $\forall \epsilon > 0\ \exists N_1 \in N : \forall n>N_1 \implies |x_n-a|< {\epsilon \over |A|}$  
   $|A_{x_1} - A_a|=|A||x_n-a| < |A|{\epsilon \over |A|}=\epsilon$
2. _TODO_
3. _TODO_
4. _TODO_

- [[math.calculus.monotonic-seq]]

- [[math.calculus.nested-intervals]]

- [[math.calculus.inf-sup]]

### Теорема Больцано-Вейерштрасса

Для всякой ограниченной последовательности $\lbrace x_n \rbrace$ существует подпоследовательность $\lbrace x_{n_k} \rbrace \subset \lbrace x_{n_k} \rbrace$, сходящаяяся к числу $a$, $\exists \lim\limits_{k \to \infty} x_{n_k}=a$

#### Пример последовательности без предела

$x_n = (-1)^n$

#### Доказательство

$\forall n, M_1 \leq x_n \leq M_2$  
Выберем $x_{n_1}$ в $[M_1, M_2]$  
Выберем $x_{n_2} : n_2 > n_1$ в одном из $[M_1, x_{n_1}]$ и $[x_{n_1}, M_2]$, в котором содержится бесконечное число элементов  
[[Принцип вложенных отрезков|math.calculus.nested-intervals]], получаем предел $a$ (доказать дома)

### Предельная точка последовательности

> Определение. Точка $a$ - предельная точка последовательности $\lbrace x_n \rbrace \iff \forall \epsilon>0 \ U_\epsilon(a)$ содержит бесконечное число членов $\lbrace x_n \rbrace$

Пример случая с двумя предельными точками: $(-1)^n+{1 \over n}$

#### Задача

Пусть $\lbrace a_n \rbrace$ - произвольная последовательность. Тогда $\exists\lbrace x_n \rbrace :$ множество предельных точек $\lbrace x_n \rbrace$ содержит $\lbrace a_n \rbrace$

##### Пример

Множество $\Q$ - счётно, пусть $a \in R$ - произвольная $a = a_0 + a_1 + a_2 + ...$; $\lbrace b_n = a_0, a_1, a_2 ... \rbrace, b_n \in \Q, \lim\limits_{n \to \infty}$ b_n = a

- [[math.calculus.cauchy-seq]]
