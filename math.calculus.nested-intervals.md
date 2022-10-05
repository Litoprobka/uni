---
id: bupz6xm53onw9u4dm6044uc
title: Принцип вложенных отрезков
desc: ""
updated: 1664962596482
created: 1664955439762
---

> Теорема. Пусть $\lbrace I_n \rbrace = \lbrace [a_n, b_n] : \forall n \implies I_{n+1} \subset I_n \rbrace$, причём $\exists \lim(b_n-a_n)=0$.  
> Тогда $\exists! c \in \R : c = \bigcap [a_n,b_n]$

## Доказательство

$a_1 \leq a_2 \leq b_k \leq b_{k-1} \leq ... \leq b_1$  
Следовательно $\lbrace a_n \rbrace$ - неубывает и ограничена любым $b_i$ $\implies \exists \lim a_i=a_0 \implies a_0 \leq b_i \forall i \implies \lbrace b_k \rbrace -$ невозрастает и ограничена снизу $a_0 \implies \exists \lim b_k=b_0 \implies a_0 \leq b_0$

Докажем, что $a_0=b_0$.  
От противного. $[a_0, b_0] \subset [a_k, b_k] \forall k \in \N$ и $b_0-a_0 > 0$ - противоречие, т.к. $\exists k : b_k < a_k < b_0 - a_0 \implies a_0 = b_0$
