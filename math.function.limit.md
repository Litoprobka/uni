---
id: umty1l5b06sgdia0duo93qm
title: Предел функции
desc: ""
updated: 1665144016336
created: 1664951149511
---

$f(x)={x^2 - 3x + 2 \over x -1}, x \neq 1$  
$f(x)={(x-1)(x-2) \over (x-1)} = x-2 \to -1$

## Определения

> Определение. Число $A$ называется пределом функции $f(x)$ при $x \to a$, если $\forall \epsilon > 0 \exists \delta > 0 : \forall x : 0 < |x-a| < \delta \implies |f(x)-A|<\epsilon$
>
> $A = \lim f(x) \iff \forall U(A) \exists \dot U(a) : \forall x \in \dot U(a) \implies f(x) \in U(A)$  
> (доказать эквивалентность определений)

> Определение. Oкрестностью точки $a$, $U(a)$, называется любое подмножество $U(a) \subset \R : \exists U_\epsilon(a) \subset U(a)$ -_какой $\epsilon$ имеется в виду?_l

> Определение. Проколотой $\epsilon$-окрестностью точки $a$ называется $\dot U_\epsilon = \lbrace x \in \R : 0 < |x - a| < \epsilon \rbrace; \dot U(a)=U(a) \setminus \lbrace a \rbrace$

> Определение предела по Гейне. Число $A$ называется пределом $f(x)$ при $x \to a \iff \forall \lbrace x_n \rbrace : \exists \lim\limits_{n \to \infty} x_n=a   \exists \lim\limits_{n \to \infty} f(x_n)=a$

## Теорема об эквивалентности определений

Теорема. Определение предела функции по Коши эквивалентно определению предела функции по Гейне.

### Доказательство

- $\exists \lim\limits_{x \to a} f(x)=A \implies \forall \epsilon>0 \exists \delta_\epsilon>0 : \forall x : 0 < |x-a| < \delta_\epsilon \implies |f(x)-A| < \epsilon,$ пусть $\lbrace x_n \rbrace : \lim\limits_{n \to \infty} x_n=a \implies \exists N_{\delta_\epsilon} \in \N : \forall n> N_{\delta_\epsilon} \implies |x_n-A|<\delta_\epsilon \implies \lim\limits_{n \to \infty} f(x_n)=A$
- От противного: пусть $f(x)$ имеет предел по Гейне, но не имеет предела по Коши. $\exists \epsilon_0 : \forall \delta > 0 \exists x_\delta : |x_\delta - a| < \delta \land |f(x_\delta)-A| \geq \epsilon_0$  
  Пусть $\lbrace \delta_n \rbrace = \lbrace {1 \over n} \rbrace,$ тогда $\forall \delta_n=1/n \exists x_n : |x_n-a|<\delta_n=1/n \land |f(x)-A| \geq \epsilon_0$  
  Рассмотрим $\lbrace x_n \rbrace : \lim\limits_{n \to \infty} x_n=a,$ тогда (предел по Гейне) $\implies \exists \lim\limits_{n \to \infty} f(x_n)=A$  
  $\forall n \implies |f(x_n)-A| \geq \epsilon_0 - противоречие \implies$ существует предел по Коши.

## Свойства

1. Пусть $\exists \lim\limits_{x \to a} f(x)=A, A \in R$, тогда $\exists \dot U(a) :$ в $\dot U(a)$ функция $f(x)$ ограничена.  
   Доказательство. Для $\epsilon = 1 \implies \exists \delta_0 : \forall x \in \dot u_\delta(a) \implies f(x) \in U_1(A) \iff |f(x)-A| < 1 \iff A-1 < f(x) < A+1$
2. Пусть $\exists \lim\limits_{x \to a} f(x)=A, A \in \R, A \neq 0$. Тогда $\exists \dot u(a) : \forall x \in \dot u(a) \implies |f(x)| > {|A| \over 2}$  
   Доказательство. Пусть $\epsilon = {|A| \over 2},$ тогда $\exists \delta>0 : \forall x \in \dot u_\epsilon(a) \implies |f(x)-A| < {|A| \over 2} \iff A - {|A| \over 2} < f(x) < A + {|A| \over 2}$
   $$
   \begin{cases}
   A>0 \iff A/2 < f(x) < 3A/2 \\
   A<0 \iff 3A/2 < f(x) < A_2
   \end{cases}
   $$
   $\implies |f(x)| > |A|/2$
3. Пусть $\exists \lim\limits_{x \to a} f(x)=A, \lim\limits_{x \to a} g(x)=B,$ причём $f(x) \leq g(x)$ в $\dot U(a),$ тогда $A \leq B$.  
   Доказательство. Пусть $\lbrace x_n \rbrace : \exists \lim\limits_{n \to \infty} x_n=a,$ тогда $\exists \lim\limits_{n \to \infty} f(x_n)=A, \lim\limits_{n \to \infty} g(x_n)=B$ и $\forall n \implies f(x_n) \leq g(x_n)$
4. Пусть $f(x) \leq h(x) \leq g(x)$ в $\dot u(a),$ причём $\exists \lim\limits_{x \to a} f(x)=\lim\limits_{x \to a} g(x)$. Тогда $\exists\lim\limits_{x \to \a} h(x) = \lim\limits_{x \to a} f(x)$  
   Доказательство. Пусть $x_n \to a$ при $n \to \infty$; тогда $\forall n \implies f(x_n) \leq h(x_n) \leq g(x_n),$ причём $\exists \lim\limits_{n \to \infty} f(x_n)=\lim\limits_{n \to \infty}g(x_n) \implies$ TODO

## Примеры

- Первый замечательный предел. $\lim\limits_{x \to 0} {\sin x \over x} = 1$  
  (рис. 1) ${AC \over OA} = \sin x = AC; \tg x = {BD \over OB} = BD; BD > AC; S_{\triangle OAB} < S_{OAB} < S_{\triangle ODB} \iff {1*AC \over 2} < {x*1 \over 2} < {BD \over 2} \iff \sin x < x < \tg x \implies 1 < x / \sin x < 1 / \cos x \implies \exists\lim\limits_{x \to 0} {x \over \sin x} = 1$
- Второй замечательный предел. $\lim\limits_{x \to 0}(1+x)^{1/x}=e=\lim\limits_{y \to 0}(1+1/y)^y; \exists \lim\limits_{n \to \infty} (1 + 1/n)^n = e, n \in N$  
  Доказательство. $(1+{1 \over [y] + 1})^[y] \leq (1 + 1/y)^y \leq (1 + 1/[y])^{[y]+1}$... TODO

---
*опоздал на пару, первую теорму надо будет переписать у кого-нибудь*
Теорема. Пусть $f(x)$ монотонна и непрерывна на $[a, b], $

$$
f : [a, b] \to [f(a), f(b)]\ y_1 < y_2 \in [f(a), f(b)] \\
\exists x_1, x_2 \in [a, b] : f(x_1) = y_1 < f(x_2) = y_2 \implies x_1 < x_2 \\
\text{Пусть } x \in [a, b]...$$

> Следствие: обратные функции $\arcsin x, \arccos x, \arctg x, \arcctg x$ - непрерывные

## Экпонента и логарифм

> Определение. Пусть $x \in \R$. $a^x = {\sup a^q \atop q \leq x q \in \R} (a>1)$

### Свойства

- $a^x > 0$

- $a^xa^y = a^{x + y}$
- $f(x)=a^x -$ непрерывная

#### Доказательства

1. $$\forall x\ \exists q < x \in \R (a^q > 0 \implies a^x > 0)$$
2. Пусть $x+y=z,$ пусть $\gamma \in \Q : \gamma < z \implies \gamma < x + y \iff x > \gamma - y$  
Выберем $x_0 \in \Q : x > x_0 > \gamma - y,$ пусть $у_0=\gamma-x_0$, тогда $y_0 = \gamma - x_0 < y$ и $y_0 \in \q$  
$x_0 < x, y_0 < y, x_0 + y_0 = \gamma \implies a^x = {\sup a^\gamma \atop \gamma < z, \gamma \in \Q} = {a^{x_0 + y_0} \atop x_0<x, y_0<y, x_0, y_0 \in \Q} = ... = a^xa^y$  

##### Задача

  Пусть $\forall M, N \subset \R, \forall x \in M, y \in N \implies x \geq 0, y \geq 0\ \exists K : x \leq K, y \leq k$  
  *решить самим, а мы используем это в доказательстве*
3.
  Лемма I. $\lim\limits_{n \to \infty} \ ^n \sqrt n = 1$  
  Доказательство: пусть $\lambda > 0: (1 + \lambda)^n = 1 + \lambda n + \dots > 1 + {n(n-1)\lambda \over 2},$ пусть $\lambda = ^4 \sqrt{n-1} \implies \dots \implies 1 < ^n \sqrt n < 1 + \sqrt{2 \over n} \implies \lim\limits_{n |to \infty}\ ^n\sqrt n = 1$  
  Лемма II. $\exists \lim\limits{x \to 0} a^x = 1$  
  Доказательство. Заметим, что $a^{1 \over n} < n^{1 \over n} \to 1$  
  $\lbrace {1 \over n} \rbrace$ Пусть $\lbrace x_n \rbrace : \lim\limits{n \to \infty} x_n=0;$ пусть $k_n=[1 \over x_n] < {1 \over x_n} \implies x_n < {1 \over k_n},$ причём когда ${x_n \atop n \to \infty} \to 0 \implies k_n \to +\infty \implies ... \implies$ по Гейне $\lim\limits_{a \to +0}a_x = 1 \implies \lim\limits_{a \to +0}a_x$

  Доказательство свойства 3. Пусть $x_0 \in \R$ для $\epsilon>0\ \exists \delta > 0 : |forall |\delta x|<\delta \implies |a^{\delta x} - 1| < {\epsilon \over a^{x_0}}$. Тогда $|a^{x_0+\delta x} - a^x| = a^{x_0}|a^{\delta x} - 1| < a^{x_0}{\epsilon \over a^{x_0}} = \epsilon \implies a^x$ непрерывна в $x_0$

## Равномерная непрерывность

Определение. $f(x)$ равномерно непрерывна на $M \subset \R \iff \forall \epsilon > 0\ \exists \delta > 0 : \forall x', x'' \in M : |x'-x''| < \delta \implies |f(x')-f(x'')| < \epsilon$

> Следствие. $f(x)$ равномерно-непрерывна на $M$, то $f(x)$ непрерывна на $M$.  
Замечание: обратное не верно  
Пример: пусть $M = (0; 1), f(x) = 1/x$ - непрерывна на \M  
$\exists \epsilon_0 > 0 : \forall \delta > 0\ \exists x', x'' \in M : |x'-x''| < \delta \implies |f(x')-f(x'')| > \epsilon$  
Пусть $\epsilon_0 = 1, \lbrace \delta_n \rbrace = 1/n, x'_n = {1 \over 2n}, x''_n = {1 \over 2(n+1)}; |f(x')-f(x'')| = |2n - 2(n+1)| = 2 > 1$

### Теорема Кантора

*"на отрезке определения неперывности и равномерной непрерывности совпадают"*  
$f(x)$ непрерывна на $[a, b] \implies f(x)$ равномерно непрывна на $[a, b]$

#### Доказательство

От противного: пусть $f(x)$ непрерывна на $[a, b]$ и не равномерно-непрерывна на $[a, b]$  
Тогда $\exists \epsilon_0 > 0 : \forall \delta_n=1/n : x'_n, x''_n : |x'_n-x''_n| < 1/n = \delta n \land |f(x'|n)-f(x''_n)| > \epsilon_0$  
Имеем: $\lbrace x'_n \rbrace$ - ограниченная $\implies \exists \lbrace x'_{n_k} \rbrace :$ для неё существует предел $c$, лежащий на отрезке.  
Рассмотрим $\lbrace x'_{n_k} \rbrace \implies ... \implies$ предел также равен $c$, но $f(x)$ непрерывна в $c \implies \lim\limits_{k \to \infty} f(x'_{n_k}) = f(c) = \lim\limits_{k \to \infty} f(x''_{n_k}),$ но $|f(x'_{n_k})-f(x''_{n_k})| > \epsilon$

## Бесконечно большие и бесконечно малые функции

Определение. $f(x)$ - бесконечно малая при $x \to a \iff \exists\lim\limits_{x \to a} f(x) = 0$  
$f(x)$ - бесконечно большая при $x \to a \iff \exists\lim\limits_{x \to a} |f(x)х| = \infty$

### Примеры

- $x \to 0 : x^\alpha, \sin x, \tg x, a^{x - 1} \log_a(1+x) \dots$

### Пределы

- $\lim\limits_{x \to 0} \log_a(1+x)/x = \lim\limits_{x \to 0} \log_a(1+x)^{1 \over x} \log_a\lim\limits_{x \to 0}{1+x}^{1 \over x} = \log_a e = {1 \over \ln a}$  
$\lim\limits_{x \to 0} \ln(1+x)/x = 1$

- $\lim\limits_{x \to 0} {a^{x-1} \over x} = \lim\limits_{y \to 0} {y \over \log_a(1+y)} = $

### Эквивалентность

> Бесконечно малые функции при $x \to a,\quad \alpha(x) \sim \beta(x) \iff \exists \lim\limits_{x \to a}=1$

#### Примеры

$x \to 0, x \sim \sin x \sim \tg x \sim \ln(1+x) \sim e^x - 1$  
$x^2 \sim 2(1-\cos x)$

### Порядок малости (роста)

> Бесконечно малая $\alpha(x)$ имеет порядок малости относительно бесконечно малой функции $\beta(x)$, равный $k$, если существует $\lim\limits_{x \to а} {\alpha(x) \over \beta^k(x)}=A, A \neq 0, A \in \R$

#### Примеры

1. $x, x^2, x^3 -$ бесконечно малые функции при $x \to 0 \quad \lim\limits_{x \to 0} {x^2 \over x} = 0$  
2. $(1 - \cos x)$ имеет порядок малости $=2$ относительно $\beta(x)=x$

### ???

$\alpha(x)$ и $\beta(x)$ находятся в отношении
$$\begin{cases}
\alpha(x) = O(\beta(x)), \text{ если } \exists \lim\limits_{x \to a} {\alpha(x) \over \beta(x)}=A, A \neq 0 \\
\alpha(x)=o(\beta(x)), \text{ если } \exists \lim\limits_{x \to a} {\alpha(x) \over \beta(x)}=0
\end{cases}$$

---
*тут должен быть пример*

---

Пусть $\exists\lim\limits_{x \to a} f(x)\alpha(x)$=, где $\alpha(x)$ - бесконечно малая при $x \to a$  
Тогда:

1. $\beta(x) \sim \alpha(x) \iff \lim\limits_{x \to a} f(x)\alpha(x)=\lim\limits_{x \to a}f(x)\beta(x)$
2. $\dots \lim\limits_{x \to a}{f(x) \over \alpha(x)} = \lim\limits_{x \to a}{f(x) \over \beta(x)}$

#### Доказательство

1. $$\lim\limits_{x \to a} = \lim\limits_{x \to a}f(x)\alpha(x)\lim\limits_{x \to a}\{\beta(x) \over alpha(x)}=\lim\limits_{x \to a}f(x) \beta{x} = \lim\limits_{x \to a}f(x)\beta(x)$$
2. аналогично
