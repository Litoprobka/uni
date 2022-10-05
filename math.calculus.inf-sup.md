---
id: qf2cd61adv117hqxd2suwlq
title: Точная нижняя / верхняя граница (infimum / supremum)
desc: ""
updated: 1664962549815
created: 1664955311420
---

## Определения

> Число $M$ называется точной верхней (нижней) гранью числового множества $X \subset \R$, если:

1. $\forall x \in X \implies x \leq M$ $(x \geq M)$
2. $\forall \epsilon > 0 \exists x_\epsilon \in X : M-\epsilon < x_\epsilon \leq M$ $(M \leq x_\epsilon < M)$
   > т.е. $M$ ограничивает $X$ и является наименьшим (наибольшим) числом, которое его ограничивает  
   > Записывается $M = \sup X$ $(M = \inf X)$

### Пример

$\sup (0;1) = 1, \inf (0;1) = 0$

## Теорема

Всякое ограниченное сверху (снизу) множество $X$ имеет точную верхнюю (нижнюю) границу.

### Доказательство

Пусть $M \geq x\ \forall x \in X$  
Пусть $x_0 \in X$

- Рассмотрим отрезок $I_1=[x_0, M]$
- Разделим $I_1$ пополам, назовём точку $M_1$
- Выбираем из $[x_0, M_1]$ и $[M_1, M]$ самый правый, содержащий элементы множества $X$
- Rinse and repeat  
  ...
- Получаем [[систему вложенных отрезков | math.calculus.nested-intervals]] $I_1 \subset I_2 \subset I_3...$ - их длины стремятся к 0 $\implies \exists M_0 = \bigcap I_k$  
  Покажем, что $M_0$ - точная верхняя грань.
  - От противного. Пусть $\exists x_0 \in X : x_0 > M_0 \implies \exists I_k \ni M_0 : I_k < x_0 \implies$ противоречие
  - Пусть $M_0 - \epsilon < M_0 \implies \exists I_k \ni M_0 : I_k > M_0-\epsilon \implies \exists x_k \in X : x_k \in I_k \implies x_k > M_0 - \epsilon \implies M_0 - \epsilon$ не является верхней гранью $\implies$ чтд.
