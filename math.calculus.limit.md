---
id: ar9abllhc7rlg1rgm3r1wqe
title: Последовательность. Предел последовательностиmit
desc: ''
updated: 1663272850459
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

#### Докозательства
1. $\forall \epsilon > 0 \space \exists N_1 \in N : \forall n>N_1 \implies |x_n-a|< {\epsilon \over |A|}$  
$|A_{x_1} - A_a|=|A||x_n-a| < |A|{\epsilon \over |A|}=\epsilon$  
2. *TODO*
3. *TODO*
4. *TODO*