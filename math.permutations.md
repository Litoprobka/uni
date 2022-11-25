---
id: tl2h18rcy7uj61sxp36bgif
title: Permutations
desc: ''
updated: 1669127044823
created: 1668420213513
---

$X$ - множество  
$S(X) = \lbrace f : X \to X, f - \text{биекция} \rbrace$  
$\forall f, g \in S(X)\quad f \circ g \in S(X)$

$ord(a)$ = наименьшее $n \in \N : f^n = Id$

> цикл - $f \in S(X) : f(k_i) = k_{i+1},\ i = 1, 2, \dots, l-1$  
> записывается $(k_1, k_2, \dots, k_l)$

$$
f = (k_1 \dots k_l) \\
g = (s_1 \dots s_l) \\
{k_i} \sqcup {s_j} \\
\implies f \circ g = g \circ f \\
\text{ $f$ и $g$ - независимые циклы}
$$

## Теорема

Любую перестановку можно однозначно представить в виде композиции независимых циклов
$$
(^{1234567}_{2574163}) = (125)(37)
$$

Для независимых циклов $(fg)^m = f^mg^m$  
$ord(f \circ g) = НОК(ord\ f, ord\ g)$

## $S_3$

$$\begin{align}
& Id - 1 \
& (ij) - 3\ (\text{транспозиции})\ & ord = 2 \\
& (ijk) - 2 & ord = 3 \\
\end{align}$$

## $S_4$

$$\begin{align}
& Id - 1 \\
& (ij) - 6 & ord = 2 \\
& (ijk) - 8 & ord = 3 \\
& (ijkl) - 6 & ord = 4 \\
& (ij)(kl) - 3 & ord = 2
\end{align}$$

---

$$
f = \begin{pmatrix}
1 & 2 & \dots & n \\
i_1 & i_2 & \dots & i_n
\end{pmatrix}
$$

Чётность перестановки $f$ - чётность числа инверсий в ней (или чётность разложения переста новки на транспозиции)  
Инверсия - такие элементы $a$ и $b$, что до перестановки $a$ идёт перед $b$, а после перестановки - после

Сопоставим перестановке $f$ матрицу $A_f : A_{f\ i_kk} = 1$
$$
\begin{pmatrix}
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix}
$$
Другое определение инверсии - *TODO (квадрат)*

## Чётность разных перестановок

$\epsilon(f) = 1 \iff f \text{ чётная, иначе } -1$

* $\epsilon((ij)) = -1$, т.к. все элементы кроме $i$ и $j$ лежат на главной диагонали $A_{(ij)} \implies \text{инверсий} (i - j - 1) * 2 + 1$

### Теорема

$\epsilon(f)\epsilon(g) = \epsilon(fg)$

## Теорема

Любая перестановка может быть представлена как композиция транспозиций

> Умножение на транспозицию меняет чётность перестановки
> $$
\epsilon(f)=-\epsilon((ij)f) \\
\implies \text{ для } f = \displaystyle\prod_{i = 1}^N t_i \quad \epsilon(f) = (-1)^N
> $$

## Чётность цикла

> Теорема: цикл чётен $\iff$ длина цикла чётна  
> Лемма: цикл длиной $n$ можно разложить на транспозиции $(1, 2)(1, 3)\dots(1,n)$

## Доказательство

### База

$
n = 2 \\
(1, 2) = (1, 2)\blacksquare
$

### Шаг

$(1, 2, \dots, n) = (1, 2)(1, 3)\dots(1,n)$  
Проверяем: $(1, 2, \dots, n+1) = (1, 2)(1, 3)\dots(1,n+1) \iff (1, 2, \dots, n+1) = (1, 2, \dots, n)(1, n+1)$  
После перестановки $(1, n+1)$ элемент $1$ стоит на позиции $n+1$.

Перестановка $(1, 2, \dots, n)$ сдвигает элементы со второго по $n$-ый на одну позицию и сдвигает последний элемент, $1$, на $(n-1)$ элементов влево, т.е. $1$ встаёт на позицию $(n+1)-(n-1)=2$.

Итого: $n + 1$ на первой позиции, $1$ на второй, элементы с третьего по $n$-ый сдвинуты
вправо на одну позицию $\iff (1, 2, \dots, n+1) = (1, 2, \dots, n)(1, n+1) \blacksquare$

## $A_{f \circ g} = A_fA_g$

### Доказательство

$$
(A_fA_g)_{ij} = \displaystyle\sum_{k=1}^n (A_f)_{ik} (A_g)_{kj} =
\begin{cases}
\exists k : (A_f)_{ik} = 1 \land (A_g)_{kj} =1 \iff f(i) = k \land g(k) = j \implies 1 \\
\nexists k : \dots \implies 0
\end{cases} \\
\iff (A_fA_g)_{ij} = A_{f \circ g}
$$

$$
\begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix}
= \begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0

\end{pmatrix}
$$

## "Игорь Вадимович попросил меня дать вам стрёмное доказательство, которое я сам не понял, но оно ему очень нравится"

*развод, нам дадут более простое доказательство*  

Любая транспозиция меняет чётность.

> Лемма: транспозиция двух соседей меняет чётность перестановки

Замена либо увеличивает число инверсий на одну, либо уменьшает $\implies$ чётность меняется

### Доказательство

Любую транспозицию можно разложить на $2S+1$ транспозиций соседних элементов, где $S$ - число элементов между меняемыми местами
$$
a, i_1, i_2, i_3, \dots, i_S, b \\
\text{применим } (a, b)\dots(i_2, a)(i_1, a) - S+1 \text { перестановок} \\
i_1, i_2, \dots, i_S, b, a \\
\text{применим } (i_1, b)\dots(i_{S-1}, b)(i_S, b) - S \text { перестановок} \\
\implies \text{ любая транспозиция нечётна}
$$

$\implies$ чётность перестановки = чётность числа транспозиций, на которые она раскладывается

## Чётность складывается

$$
\begin{cases}
\text{Ч} \circ \text{НЧ} = \text{НЧ} & 2k + 2z + 1 \text{ транспозиций} \\
\text{НЧ} \circ \text{НЧ} = \text{Ч} & 2k + 1 + 2z + 1 \text{ транспозиций} \\
\text{Ч} \circ \text{Ч} = \text{Ч} &   2k + 2z \text{ транспозиций}
\end{cases}$$

## Перестановка раскладывается в независимые циклы

*а где доказательство?*

## Чётных и нечётных перестановок длины $n$ по ${n! \over 2}$

$$
\text{Ч} - \text{чётные перестановки} \\
\text{НЧ} - \text{нечётные перестановки} \\
$$

Транспозиция меняет знак, перестановки биективны $\implies (1, 2) \circ$ - биекция между Ч и НЧ $\implies |\text{Ч}| = |\text{НЧ}|$

---
$$
G = \ni g_1, g_2, \exists h \in G : g_1 = hg_2h^{-1} \iff \text{$g_1$ и $g_2$ сопряженные} \iff \text{$g_1$ и $g_2$ эквивалентны}
$$

* рефлексивность - $ege^{-1}$
* транзитивность - $g_1 = hg_2h^{-1},\ g_2 = hg_3k^{-1} \implies g_1 = hkg_3k^{-1}h^{-1} \iff g_1 = hkg_3(hk^{-1})$
* симметричность - $a = gbg^{-1} \implies? b = g^{-1}ag\quad g^{-1}a = (g^{-1}g)bg^{-1} \iff g^{-1}a = bg^{-1} \iff g^{-1}ag = bg^{-1}g \iff g^{-1}ga = b$

---
> чётность перестановки $=$ знак определителя её матрицы