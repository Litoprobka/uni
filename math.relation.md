---
id: zt56k0ul6q1cvl1mmco368z
title: Relation
desc: ''
updated: 1666275250284
created: 1666272319420
---

Отношения - это обобщение функций. В отличие от функций, у элемента "домена" отношения может не быть или быть несколько "прообразов".

Отношение $R$ на множествaх $А$ и $B$ записывается $R \subset A \times B$  
*"Думайте об отношениях как о подмножествах, и ваша жизнь станет легче" - дословно цитату я не запомнил, что-то в этом роде*

Для $(x, y) \in R$ ($x$ и $y$ находятся в отношении $R$) есть краткая запись: $xRy$

## Примеры

* $X = \lbrace 1, 2, 3, 6 \rbrace$  
  делимость - $R = \lbrace (x, y) : y|x\ \forall x, y \in X \rbrace$
* $R \subset \R \times \R$, отношение - $x < y$ (график - верхний треугольник)
* $S \subset R \times R, S = \lbrace (x, y) : |x - y| \leq 1 \rbrace$
* $M$ - множество мужчин, $F$ - множество женщин, $\Omega = M \cap F$ - множество всех людей,  
  $xRy$ - $x$ родитель $y$, $xSy$ - $x$ супруг $y$
  * $x$ отец $y \iff x(R \cap (M \times \Omega))y$
  * $x$ дедушка/бабушка $y \iff x(R^{-1} \circ R)y$
  * $x$ бабушка $y \iff x((F \times \Omega) \cap (R \circ R))y$
  * $x$ брат / сестра $y \iff x(R^{-1} \circ R)y$
  * у $x$ и $y$ одна мать $\iff x((R^{-1} \cap (\Omega \times F)) \circ R)y$
  * $x$ - парень, $y$ - девушка, $x$ и $у$ родные брат и сестра  
  $\iff x(((R^{-1} \cap (M \times M)) \circ R) \cap
           (R^{-1}                    \circ (R \cap (F \times F)))y$  
  *помогите, какой приоритет у $\times$, $\cap$ и $\circ$?*

## Свойства отношений

* функциональность - $\forall x, y, z\quad xRy \land xRz \iff y = z$
* $R$ всюду определено - $\forall x \in A\ \exists y \in B : xRy$
  * $R$ функционально и всюду определено $\implies R$ - функция
* инъективность и сюръективность - [[те же определения | math.function#инъективность-мономорфизм]], что и для функций
  * биективность - $R$ биективно $\iff$ $R$ - функция, $R$ инъективно и сюръективно
* симметричность - $\forall x, y\ (xRy \iff yRx)$
  * антисимметричность - $\forall x, y \quad xRy \land bRa \implies a = b$
  * ассиметричность - $\forall x, y \quad xRy \implies \lnot yRx$
* рефлексивность - $\forall x\ xRx$ (подразумевает $A = B$)
* транзитивность - $\forall x, y, z\quad xRy \land yRz \implies xRz$
* $R$ - отношение эквивалентности $\iff R$ симметрично, рефлексивно и транзитивно  
  * пример - $B = A = A_1 \sqcup A_2 \sqcup \dots \sqcup A_m$  
  $xRy \iff \exists i : x \in A_i \land y \in A_i$
  * такие $R$ обычно обозначают $\sim$

## Обратное отношение

В отличие от функций, обратное отношение существует для любого отношения

$xRy \iff yR^{-1}x$

## Композиция отношений

Записывается как композиция функций: $R \circ Q$  
$$\forall R \subset A \times B, Q \subset B \times C \quad R \circ Q =
  \lbrace (x, y) \in A \times C : \exists z \in B : xRzQy \rbrace \\
  (R \circ Q)^{-1} = R^{-1} \circ Q^{-1}
$$

Иными словами, $x(R \circ Q)y$ $\iff$ существует такой промежуточный элемент $z$, что $xRz$ и $zQy$

### Теорема об отношениях эквивалентности

Теорема. Любое отношение эквивалентности на $X$ получается из какого-то разбиения $X$ на подмножества  
Доказательство. Дано $R \implies \forall a\ X_a = \lbrace b \in X : bRa \rbrace$; $X_a -$ класс эквивалентности элемента $a$  
$\forall a, b \in X : X_a = X_b \lor X_a \sqcup X_b$  
Пусть $\exists c \in X_a \cup X_b \implies cRa \land cRb \implies aRc \implies aRb$  
$\forall z \in X_a \implies zRa \implies zRb \implies z \in X_b$
