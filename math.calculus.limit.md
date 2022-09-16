---
id: ar9abllhc7rlg1rgm3r1wqe
title: Последовательность. Предел последовательности
desc: ''
updated: 1663352827162
created: 1663265851396
---

## Определение последовательности
*Я пропустил эту часть лекции, так что вот определение с Википедии*

Пусть задано множество $X$.  
Всякое отображение $f : \N \to X$ называется последовательностью элементов множества $X$.

## Определение предела
> Число $a \in R$ называется пределом последовательности $\lbrace x_n \rbrace$, если $\forall \epsilon >0 \exists N_\epsilon \in \N : \forall n > N_\epsilon \implies |x_n - a| < \epsilon$ и записывается $\lim\limits_{n \to \infty} x_n = a$

$U_\epsilon(a) = \lbrace x : |x - a| < \epsilon \rbrace$ - $\epsilon$-окружность

> Число $а=\lim\limits_{n \to \infty} x_n$, если $\forall \epsilon > 0$ вне окрестности $U_\epsilon(a)$ содержится конечное число членов последовательности $\lbrace x_n \rbrace$

## Примеры
* $\lim\limits_{n \to \infty} {1 \over n}=0$  
$|{1 \over n} - 0| < \epsilon \implies n > {1 \over \epsilon} \implies N_\epsilon=[{1 \over \epsilon}]$
* $\lbrace q^n \rbrace, 0<q<1 \\  
\lim\limits_{n \to \infty} q^n = 0 \\
|q^n-0|<\epsilon \implies q^n < \epsilon \implies 
n \ln q < \ln \epsilon \implies n > {\ln \epsilon \over \ln q}, N_\epsilon=[{\ln \epsilon \over \ln q}]$

> $X_n$ - ограниченная, если $\exists M> : \forall n \in \N \implies |X_n| >0$

## Свойства пределов последовательности

1. > $\exists \lim\limits_{n \to \infty} x_n=a \implies \exists! \lim\limits_{n \to \infty} x_n=a$

    Доказательство: пусть $b=\lim\limits_{n \to \infty} x_n, b \neq a \\
    \epsilon \in \R: U_\epsilon(b) \cap U_\epsilon(b) = \emptyset \implies$ противоречие

2. > $\exists \lim\limits_{n \to \infty} x_n=a, a \in \R,$ то $\lbrace x_n \rbrace$ - ограниченная

    Доказательство: для $\epsilon = 1\,\exists N_1 \in \N : \forall n>N_1 \implies |x_n-a| < 1 \implies x-1 \leq x_n \leq x + 1$, тогда $M = max \lbrace |x_1|, |x_2|...|x_n|, |a-1|, |a +1| \rbrace$

3. > $\exists \lbrace x_n \rbrace, \lbrace y_n \rbrace : x_n \leq y_n \forall n \in \N \implies \text{если } \exists \lim\limits_{n \to \infty} x_n=a, \lim\limits_{n \to \infty} y_n=b,$ то $a \leq b$

    Доказательство: *TODO*

4. > $\exists \lim\limits_{n \to \infty} x_n=a, a\neq 0 \implies \exists N_0 \in \N : (\forall n>N_0\ \implies |x_n| > {|a| \over 2})$

    Доказательство:  
    Пусть $\epsilon = a/2 \implies \exists N_0 \in \N : \forall n \in \N : n > N_0 \implies |x_n - a| < {|a| \over 2} \iff -{|a| \over 2} < x_n -a<{|a| \over 2} \implies a - {|a| \over 2} < x_n < a + {|a| \over 2}$

    Если $a > 0$: ${a \over 2} < x_n < {3a \over 2}$  
    Если $a < 0$: $x_n < {a \over 2} \implies |x_n| > {|a| \over 2}$

5. > $x_n<y_n<z_n, \exists \lim\limits_{n \to \infty} x_n = \lim\limits_{n \to \infty} z_n = a \implies \exists \lim\limits_{n \to \infty} y_n = a$. 

    Доказательство: *TODO*

### Арифметические действия с предельными последовательностями

> Теорема 6. Пусть $a=\lim\limits_{n \to \infty} x_n, b=\lim\limits_{n \to \infty} y_n, a, b \in \R$  
Tогда:  
1. $\exists \lim\limits_{n \to \infty} Ax_n = Aa, \forall A\in\R$
2. $\exists \lim\limits_{n \to \infty} (x_n+y_n) = a + b$
3. $\exists \lim\limits_{n \to \infty} (x_n*y_n) = a * b$
4. $b \neq 0 \implies \exists \lim\limits_{n \to \infty} (x_n/y_n) = a / b$

#### Доказательства
1. $\forall \epsilon > 0 \space \exists N_1 \in N : \forall n>N_1 \implies |x_n-a|< {\epsilon \over |A|}$  
$|A_{x_1} - A_a|=|A||x_n-a| < |A|{\epsilon \over |A|}=\epsilon$  
2. *TODO*
3. *TODO*
4. *TODO*


## Убывающие и возрастающие последовательности
> Определение  
> $\lbrace x_n \rbrace$ - возрастает (неубывает) $\iff \forall n \in \N \space \implies x_{n+1}>x_n$  
> $\lbrace x_n \rbrace$ - убывает (невозрастает) $\iff \forall n \in \N \implies x_{n+1}>x_n$

### Стабилизирующаяся последовательность 
Пусть $\lbrace x_n \rbrace$ - последовательность вещественных чисел, $x_n=b_{n1},b_{n2}...b_{nk}$, где $b_{n0}$ - целая часть дроби, $b_{ni}$ - i-ая цифра после запятой

Последовательность стабилизируется, если $\forall k\in \N \cup \lbrace 0 \rbrace \space \exists n_k \in \N : \forall n > n_k \implies b_{nk} = b^0_k$

#### Лемма о стабилизации
Пусть $\lbrace x_n \rbrace$ - неубывающая последовательность, ограниченная сверху ($\exists M : \forall n x_n < M$); тогда последователность стабилизируется

##### Доказательство
$$
x_1 = b_{10}, b_{13}...b_{1k} \\
x_2 = b_{20}, b_{23}...b_{2k} \\
... \\
x_n = b_{n0}, b_{n3}...b_{nk} \\
\text{Последовательность неубывает }\implies x_n \geq x_{n-1} \implies \exists x_{k0} : x_{k+1 0} > M
$$

### Предел неубывающей последовательности
Теорема. Всякая неубывающая (невозрастающая) последовательность $\lbrace x_n \rbrace$, ограниченная сверху (снизу) имеет предел.
#### Доказательство
Пусть $\lbrace x_n \rbrace$ неубывает, тогда по [[лемме | math.calculus.limit#лемма-о-стабилизации]] она стабилизируется к числу $b_0=b_{01},b_{02}...b_{0n}$

Пусть $\epsilon>0$, тогда $\exists n_0 \in \N : 10^{-n_0} < \epsilon$, то $\exists N_0 : \forall n > N_0 \implies x_n=b_{00},b_{01}..b_{0k} \implies |x_n-b_0| = |0,0...0 \text{n знаков}| < 10^{-n_0} < \epsilon \implies b_0=\lim\limits_{n \to \infty} x_n$

### Число e
$e = \lim\limits_{n \to \infty} (1 + {1 \over n})^n = 2,7182...$

> Теорема. $\lbrace x_n \rbrace = (1 + {1 \over n})^n$ строго возрастает и ограничена сверху

$x_n=(1 + {1 \over n})^n = 1 + n{1 \over n}+{n(n-1) \over 2}{1 \over n^2}...+{n(n-1)(n-2)...(n-k+1) \over k!}{1 \over n^k}=2 + {1 \over 2!(1 - 1/n)}+{1 \over 3!}(1- 1/n)(1 - 2/n)+...+{1 \over k!}(1-1/n)(1-2/n)...(1-(k-1)/n)+...+{1 \over n!}(1-1/n)(1-2/n)...(1-(n-1)/n)$

$x_{n+1}={1 \over 2!(1 - {1 \over n+1})}+...+{1 \over n+1!}(1-{1 \over n+1})(1-2/(n+1))...(1-n/(n+1))$ - слагаемые $x_{n+1}$ попарно больше слагаемых $x_n$

${1 \over k!} \leq {1 \over 2^{k-1}}$

$x_n < 2 + {1 \over 2!} + {1 \over 3!}+...+{1 \over n!} \leq 2 + 1/2 + 1/4 + 1/8... \implies x_n < 3 \implies \forall n \exists \lim\limits_{n \to \infty} (1+ {1 \over n}^n)=l$

#### Бином Ньютона
$(a+b)^n=a^n+na^{n-1}b+{n(n-1) \over 2}a^{n-2}b^2+...+b^n = \displaystyle\sum^n_{k=0} C^k_n a^{n-k}b^k$

Доказательство: $(a+b)^n=(a+b)(a+b)(a+b)...$ $n$ раз - $C^k_n a^{n-k}b^k$  


## Принцип вложенных отрезков
> Теорема. Пусть $\lbrace I_n \rbrace = \lbrace [a_n, b_n] : \forall n \implies I_{n+1} \subset I_n \rbrace$, причём $\exists \lim(b_n-a_n)=0$. Тогда $\exists! c \in \R : c = \bigcap [a_n,b_n]$

Доказательство.  
$a_1 \leq a_2 \leq b_k \leq b_{k-1} \leq ... \leq b_1$  
Следовательно $\lbrace a_n \rbrace$ - неубывает и ограничена любым $b_i$ $\implies \exists \lim a_i=a_0 \implies a_0 \leq b_i \forall i \implies \lbrace b_k \rbrace -$ невозрастает и ограничена снизу $a_0 \implies \exists \lim b_k=b_0 \implies a_0 \leq b_0$

Докажем, что $a_0=b_0$.  
От противного. $[a_0, b_0] \subset [a_k, b_k] \forall k \in \N$ и $b_0-a_0 > 0$ - противоречие, т.к. $\exists k : b_k < a_k < b_0 - a_0 \implies a_0 = b_0$


> Опр. число $M$ назыевается точной верхней (низней) гранью числового множества X \subset \R, если:
1. $\forall x \in X \implies x \leq M$ $(x \geq M)$
2. $\forall \epsilon > 0 \exists x_\epsilon \in X : M-\epsilon < x_\epsilon \leq M$ $(M \leq x_\epsilon < M)$
>
> т.е. $M$ ограничивает $X$ и является наименьшим (наибольшим) числом, которое его ограничивает  
Записывается $M = \sup X$ $(M = \inf X)$

#### Пример
$\sup (0;1) = 1, \inf (0;1) = 0$

### Точная граница
> Теорема. Всякое ограниченное сверху (снизу) множесво $X$ имеет точную верхнюю (нижнюю) границу.

#### Доказательство
Пусть $M \geq x \forall x \in X$  
Пусть $x_0 \in X$

Рассмотрим отрезок $I_1=[x_0, M]$  
Разделим $I_1$ пополам, назовём точку $M_1$  
Выбираем из $[x_0, M_1]$ и $[M_1, M]$ самый правый, содержащий элементы множества $X$  
Rinse and repeat  
...
Получаем систему вложенных отрезков $I_1 \subset I_2 \subset I_3...$ - их длины стремятся к 0 $\implies \exists M_0 = \bigcap I_k$  
Покажем, что $M_0$ - точная верхняя грань.  
1. От противного. Пусть $\exists x_0 \in X : x_0 > M_0 \implies \exists I_k \ni M_0 : I_k < x_0 \implies$ противоречие
2. Пусть $M_0 - \epsilon < M_0 \implies \exists I_k \ni M_0 : I_k > M_0-\epsilon \implies \exists x_k \in X : x_k \in I_k \implies x_k > M_0 - \epsilon \implies M_0 - \epsilon$ не является верхней гранью $\implies$ чтд.

### Теорема Больцано-Вейерштрасса
Для всякой ограниченной последовательности $\lbrace x_n \rbrace$ существые подпоследовательность $\lbrace x_{n_k} \rbrace \subset \lbrace x_{n_k} \rbrace$, сходящаяяся к числу $a$, $\exists \lim\limits_{k \to \infty} x_{n_k}=a$

#### Пример последовательности без предела
$x_n = (-1)^n$

#### Доказательство
$\forall n, M_1 \leq x_n \leq M_2$  
Выберем $x_{n_1}$ в $[M_1, M_2]$  
Выберем $x_{n_2}$ в одном из $[M_1, x_{n_1}]$ и $[x_{n_1}, M_2]$, в котором содержится бесконечное число элементов  
Принцип вложенных отрезков, получаем предел $a$ (доказать дома)

### Фундаментальные последовательности
> Определение. Последовательность $\lbrace X_n \rbrace$ назыевается фундаментальной последовательностью...