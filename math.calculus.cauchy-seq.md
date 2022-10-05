---
id: 5rx0zuvuo3po2kxvbuwoj4u
title: Фундаментальные последовательности (последовательности Коши)
desc: ""
updated: 1664962563608
created: 1664951860263
---

Последовательность $\lbrace X_n \rbrace$ называется фундаментальной последовательностью (последовательностью Коши), если $\forall \epsilon>0\ \exists N_\epsilon \in \N : \forall m,n>N_\epsilon \implies |x_m-x_n|<\epsilon$

## Теорема о пределе фундаментальной последовательности

$\lbrace X_n \rbrace$ - фундаментальная, $\iff \exists \lim\limits_{n \to \infty} x_n=a, a \in \R$

### Доказательство

#### Необходимость

Из определения предела получаем: $\forall \epsilon > 0\ \exists N_\epsilon \in \N : \forall n>N_\epsilon \implies |x_n-a| < {\epsilon \over 2}$  
Пусть $n,m>N_\epsilon,$ тогда $|x_n-x_m|=|(x_n-a)-(x_m-a)| < |x_n-a| + |x_m-a| < \epsilon$

#### Достаточность

Докажем, что $\lbrace X_n \rbrace$ - фундаментальная: пусть $\epsilon = 1$, тогда $\exists N_1 \in \N : \forall m,n_0>N_1 \implies |x_m-x_{n_0}| < 1 \iff -1 < x_{n_1} - x_{n_0} < 1 \iff x_{n_0}-1 < x_{n_1} < x_{n_0}+1 \implies$ вне отрезка содержится конечное число членов последовательности; по теореме Больцано-Вейерштрасса $\implies \exists \lbrace X_{n_k} \rbrace \subset \lbrace X_n \rbrace : \exists \lim\limits_{k \to \infty}=a, a \in \R$

- $\forall \epsilon>0\ \exists N_1 : \forall m,n>N_1 \implies |x_n-x_m| < {\epsilon \over 2}$
- $\exists N_0 \forall k>N_0 \implies |X_{n_k}-a| < {\epsilon \over 2}$

Пусть $N=$ что-то $\lbrace N, n_{n_0} \rbrace$, тогда $\forall n > N \implies |x_n-a|=|x_n-x_{n_k}+x_{n_k}-a| < |x_n-x_{n_k}|+|x_{n_k}-a| < \epsilon$
