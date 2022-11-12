---
id: g3gj4llkolbtwta94a6j9r6
title: Теорема Кантора
desc: ''
updated: 1555548393067
created: 1555548393067
---

> $|A|$ имеет меньшую мощность, чем $|2^A|$

## Доказательство
* для конечных множеств: $\forall n \in \N \cup \lbrace 0 \rbrace\ 2^n > n \implies |2^A| > |A|$
* для бесконечных множеств:  
Предположим, что $A$ равномощно $2^A$. Тогда существует биекция $f : A \to 2^A$  
Рассмотрим $B  \lbrace x \in A : x \notin f(x) \rbrace$  
$f$ биективна, $B \subset A$ $\implies \exists y \in A : f(y) = B \implies$ противоречие $\implies f$ не биективна и не сюръективна
С другой стороны, $g : A \to 2^A, g(x) = \lbrace x \rbrace$ инъективна $\implies$ мощность $A$ меньше мощности $2^A$