---
id: oy9udnwtv0skgz5y2p07kz8
title: Убывающие и возрастающие последовательности
desc: ''
updated: 1666360117270
created: 1664958436510
---
> Определение  
> $\lbrace x_n \rbrace$ - возрастает (неубывает) $\iff \forall n \in \N\ \implies x_{n+1}>x_n$  
> $\lbrace x_n \rbrace$ - убывает (невозрастает) $\iff \forall n \in \N\ \implies x_{n+1}>x_n$

## Стабилизирующаяся последовательность

Пусть $\lbrace x_n \rbrace$ - последовательность вещественных чисел, $x_n=b_{n0},b_{n1},b_{n2}...b_{nk}$, где $b_{n0}$ - целая часть дроби, $b_{ni}$ - i-ая цифра после запятой

Последовательность стабилизируется, если $\forall k\in \N \cup \lbrace 0 \rbrace\ \exists n_k \in \N : \forall n > n_k \implies b_{nk} = b^0_k$

### Лемма о стабилизации

Пусть $\lbrace x_n \rbrace$ - неубывающая последовательность, ограниченная сверху ($\exists M : \forall n x_n < M$); тогда последователность стабилизируется

#### Доказательство

$$
x_1 = b_{10}, b_{13}...b_{1k} \\
x_2 = b_{20}, b_{23}...b_{2k} \\
... \\
x_n = b_{n0}, b_{n3}...b_{nk} \\
\text{Последовательность неубывает }\implies x_n \geq x_{n-1} \implies \exists x_{k0} : x_{k+1 0} > M
$$

## Предел неубывающей последовательности

Теорема. Всякая неубывающая (невозрастающая) последовательность $\lbrace x_n \rbrace$, ограниченная сверху (снизу) имеет предел.

### Доказательство

Пусть $\lbrace x_n \rbrace$ неубывает, тогда по [[лемме|math.calculus.monotonic-seq#лемма-о-стабилизации]] она стабилизируется к числу $b_0=b_{01},b_{02}...b_{0n}$

Пусть $\epsilon>0$, тогда $\exists n_0 \in \N : 10^{-n_0} < \epsilon$, то $\exists N_0 : \forall n > N_0 \implies x_n=b_{00},b_{01}..b_{0k} \implies |x_n-b_0| = |0,0...0 \text{n знаков}| < 10^{-n_0} < \epsilon \implies b_0=\lim\limits_{n \to \infty} x_n$

## Число e

$e = \lim\limits_{n \to \infty} (1 + {1 \over n})^n = 2,7182...$

> Теорема. $\lbrace x_n \rbrace = (1 + {1 \over n})^n$ строго возрастает и ограничена сверху

$x_n=(1 + {1 \over n})^n = 1 + n{1 \over n}+{n(n-1) \over 2}{1 \over n^2}...+{n(n-1)(n-2)...(n-k+1) \over k!}{1 \over n^k}=2 + {1 \over 2!(1 - 1/n)}+{1 \over 3!}(1- 1/n)(1 - 2/n)+...+{1 \over k!}(1-1/n)(1-2/n)...(1-(k-1)/n)+...+{1 \over n!}(1-1/n)(1-2/n)...(1-(n-1)/n)$

$x_{n+1}={1 \over 2!(1 - {1 \over n+1})}+...+{1 \over n+1!}(1-{1 \over n+1})(1-2/(n+1))...(1-n/(n+1))$ - слагаемые $x_{n+1}$ попарно больше слагаемых $x_n$

${1 \over k!} \leq {1 \over 2^{k-1}}$

$x_n < 2 + {1 \over 2!} + {1 \over 3!}+...+{1 \over n!} \leq 2 + 1/2 + 1/4 + 1/8... \implies x_n < 3 \implies \forall n \exists \lim\limits_{n \to \infty} (1+ {1 \over n}^n)=l$

### Бином Ньютона

$(a+b)^n=a^n+na^{n-1}b+{n(n-1) \over 2}a^{n-2}b^2+...+b^n = \displaystyle\sum^n_{k=0} C^k_n a^{n-k}b^k$

Доказательство: $(a+b)^n=(a+b)(a+b)(a+b)...$ $n$ раз - $C^k_n a^{n-k}b^k$
