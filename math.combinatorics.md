---
id: 2ongTkzfqwgbK6ktnDJMN
title: Комбинаторика
desc: ''
updated: 1667557632537
created: 1632230572756
---

- перестановки - "$n$ разных шариков в $n$ лунок", $P_n=n!$
  - частный случай размещений, $0! = 1$
- размещения - "$k$ разных шариков в $n$ лунок (или наоборот)", $k \le n;\ A_n^k={n! \over (n-k)!}$
- сочетания - "$k$ одинаковых шариков в $n$ лунок" или число $k$-элементных подмножеств $n$-элементного множества, $C_n^k=(^n_k)={A_n^k \over P^k}={n! \over (n-k)!*k!}$

---

_Дальше идёт запись первой лекции по комбинаторике в довольно хаотичной форме_

$Z_n = \lbrace 1, 2, 3, ... n \rbrace,$ подмножества $2^{Z_n}=\Omega_n$

$\Omega_n^k = \lbrace A \subset Z_n : |A| = k \rbrace, |\Omega_n^k|=C_n^k$

$\displaystyle\sum_{k=0}^n{C_n^k} = 2^n$

$$
\Omega_n^0 = \lbrace \emptyset \rbrace, C_n^0=1 \\
\Omega_n^1 = \dots, C_n^1 = n \\
\Omega_n^2 : C_n^2 = {n(n-1) \over 2} \\
\dots \\
\Omega_n^n = \lbrace Z_n \rbrace, C_n^n = 1 \\
|\Omega_n^{n-1}| = C_n^{n-1}=n
$$

В $\Omega_n^k$ и $\Omega_n^{n-k}$ одинаковое количество элементов. Докажем построением биекции:

$$
f : \Omega_n^k \to \Omega_n^{n-k} \\
f(A) = Z_n \setminus A
$$

---

$$
\Omega_{n+1}^k = \Omega_n^k \cup X \\
\Omega_n^k = \lbrace B \in \Omega_{n+1}^k : n+1 \notin B \rbrace \\
X = \lbrace B \in \Omega_{n+1}^k : n+1 \in B \rbrace, \text{остальные элементы $B$ лежат в $Z_n$} \\
\implies \text{биекция между $X$ и $\Omega_n^{k-1}$} \\
\implies C_n^k + C_n^{k + 1} = C_{n + 1}^{k + 1}
$$

$$
C_0^0 = 1 \\
C_1^0 = 1, C_1^1 = 1 \\
C_2^0 = 1, C_2^1 = 2, C_2^2 = 1 \\
C_3^0 = 1, C_4^1 = 3, C_3^2 = 3, C_3^3 = 1 \\
\dots
\\\,\\
\displaystyle{\begin{matrix} 1 \\ 1 \quad 1 \\ 1 \quad 2 \quad 1 \\ 1 \quad 3 \quad 3 \quad 1 \\
1 \quad 4 \quad 6 \quad 4 \quad 1 \\ 1 \quad 5 \quad 10 \enspace 10 \quad 5 \quad 1 \\
1 \quad 6 \quad 15 \enspace 20 \enspace 15 \quad 6 \quad 1 \\ 1 \quad 7 \quad 21 \enspace 35 \enspace 35 \enspace 21 \quad 7 \quad 1 \end{matrix}}
$$

$$
\displaystyle\sum_{k=0}^n(-1)^kC_n^k=0 - \text{нужно доказывать}
$$

$$
C_n^0 + C_{n+1}^1 + \dots + C_{n+m}^m = C_{n+m+1}^m \\
\iff \displaystyle\sum_{k=0}^mC_{n+k}^k=C_{n+m+1}^m
$$

Элементы ряда (без единиц) делятся на номер ряда, если он простой

$$
P - \text{простое}, k \neq 0, P \implies C_p^k\,\vdots\,P
$$

Правила сокращённого умножения используют треугольник Паскаля (и сочетания)  
$(a+b)^n = C_n^0a^n + C_n^1a^{n-1}b + C_n^2a^{n-2}b^2 + \dots + C_n^0b^n$ -
$(a+b)^n = \displaystyle\sum_{k=0}^n C_n^k a^{n-k}b^k$

### Доказательство бинома Ньютона

$(x + a_1)(x + a_2)\dots(x+a_n)=x^n + (n$ слагаемых с $x^1 + C_n^2 a_i x^{n-2} = (\sum a_ia_j)x^{n-2} \text{где} \lbrace i, j \rbrace \in \Omega_n^2) + (\sum a_{i_1}a_{i_2}\dots a_{i_k} : \lbrace a_i \rbrace \in \Omega_n^k)x^{n-k} + \dots + (\prod a_i)x^0$  
_множество под суммой_

#### Доказательство индукцией

_вывел его на семинаре, awww_
$$
\text{База: } \\
(a+b)^0 = 1 \\
\displaystyle\sum_{k=0}^0a^0b^0 = 1
$$

$$
\text{Шаг: } \\
(a+b)^{n+1} = (\displaystyle\sum_{k=0}^n C_n^ka^{n-k}b^k)(a + b) = \displaystyle\sum_{k=0}^n C_n^ka^{n-k}b^k(a + b) = (\displaystyle\sum_{k=0}^n C_n^ka^{n-k+1}b^k) + (\displaystyle\sum_{k=0}^n C_n^ka^{n-k}b^{k+1}) \\
\text{Заметим, что } C_n^ka^{n-k+1}b^k \text{ ($k$-ый элемент первой суммы)} + C_n^{k-1}a^{n-k+1}b^k \text{ ($(k-1)$-ый элемент второй суммы)} = C_{n+1}^ka^{n-k+1}b^k \\
\text{Попарно сложим $k$-ые элементы первой суммы с $(k-1)$-ыми второй, останется два беспарных элемента: } \\
(\displaystyle\sum_{k=1}^n C_{n+1}^ka^{n-k+1}b^k) + C_n^0a^{n+1} + C_n^nb^{n+1} \\
\text{Заметим, что } C_n^0 = 1 = C_{n+1}^0,\,C_n^n = 1 = C_{n+1}^{n+1} \\
\text{Получаем: } (\displaystyle\sum_{k=1}^n C_{n+1}^ka^{n-k+1}b^k) + C_{n+1}^0a^{n+1} + C_{n+1}^{n+1}b^{n+1} \\
= (\displaystyle\sum_{k=0}^n C_{n+1}^ka^{n-k+1}b^k) + C_{n+1}^{n+1}b^{n+1} \\
= \displaystyle\sum_{k=0}^{n+1} C_{n+1}^ka^{n+1-k}b^k\ \blacksquare
$$

#### Основные симметрические функции

$$
\sigma_1 = a_1 + a_2 + \dots + a_n \\
\sigma_2 = \displaystyle\sum_{\lbrace i, j \rbrace \in \Omega_n^2} a_ia_j = \displaystyle\sum_{1 \leq i<j\leq n} a_ia_j \\
\sigma_k = \displaystyle\sum_{1 \leq i_1 < i_2 \dots < i_k \leq n} a_{i_1}a_{i_2}\dots a_{i_k}
$$

Если $\forall i \, a_i = a_1$, то $(x+a)^n = C_n^0x^n + C_n^1x^{n-1}a + C_n^2x^{n-2}a^2 + \dots + C_n^0a^n$

#### smth

Многочлен степени $n$ от $x$ с корнями $a_1, a_2 \dots a_n$  
$(x-a_1)(x-a_2)\dots(x-a_n)$  
$\sigma_k (-а_1, -a_2, \dots, -a_n) = (-1)^k\sum a_{i_1}a_{i_2}\dots a_{i_k}$

Частный случай для кубического многочлена:  
$(x-p)(x-q)(x-r) = x^3 - (p + q + r)x^2 + (pq + qr + pr)x = pqr$

---

Одночлен (моном) $=x_1^{m_1}x_2^{m_2} \dots x_n^{m_n} = M, \deg M = \sum m_i$

Сколько есть мономов степени $k$ от $x_1 \dots x_n$  
$\iff$ "сколькими способами можно раздать $k$ яблок $n$ людям?"

Разлозим яблоки в ряд, разложим между ними соломинки; человеку 1 достаются яблоки слева от первой соломинки, второму - между первой и второй и т.д. $\implies C_{n+k-1}^k = C_{n+k-1}^{n-1}$

## Количество элементов в объединении множеств

_кидать эту лекцию в [[math.set]] или нет?_
$$
|A \cup B| \neq |A| + |B| \\
|A \cup B| = |A| + |B| - |A \cap B| \\
|A + B + C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C| \\
\text{Для большего числа множеств слишком длинно, нужна общая формула} \\
| \bigcup A_n| = \sum |A_n| - \displaystyle\sum_{\lbrace i, j \rbrace}|A_i \text{Предположение: } \cap A_j| + \displaystyle\sum_{\lbrace i, j, l \rbrace}|A_i \cap A_j \cap A_l| +  \dots + (-1)^{k+1}\displaystyle\sum_{\lbrace i_1, \dots, i_k \rbrace}|\bigcap A_{i_k}|\\
$$

$$
\chi_{A \cup B} = \chi_A + \chi_B - \chi_{A \cap B} \\
|A \cup B| = |A| + |B| - |A \cap B| \\
\text{Как перевести первое во второе?} \\
S(\chi_A + \chi_B - \chi_{A \cap B}) = S(\chi_A) + S(\chi_B) + (-1)S(\chi_{A \cap B}) = |A| + |B| - |A \cap B|
$$

### "Дискретный интеграл"

_TODO: линейность_
$$
\text{Пусть } A - \text{конечное множество} \\
f : A \to \R \\
S(f) = \displaystyle\sum_{x \in A} f(x)
$$

#### Свойства

- $S(f + g) = S(f) + f(g)$

- $\forall c \in \R\ S(c*f) = c*S(f)$
- $S(\chi_A) = |A|$

---
$$
\chi_{\bigcup A_n} = ? \\
A_1 \cup A_2 = \overline{\overline A_1 \cap \overline A_2} \\
A_1 \cup \dots \cup A_4 = \overline{\overline A_1 \cap \dots \cap \overline A_4} \\
\bigcup A_n = \overline{\overline{\overline{(\overline A_1 \cap \overline A_2 \dots)}} \cap \overline A_n} = (\overline{\overline A_1 \cap \dots \cap \overline A_{n-1}}) \cup \overline A_n\\
\chi_{\bigcup A_n} = 1 - \prod \chi_{\overline A_i} = 1 - \prod 1-\chi_{A_i} = \sum \chi_{A_i} - \sum \chi_{A_i \cap A_j} + \dots + (-1)^{k-1}\sum \chi_{\bigcap A_{i_k}} \\
\iff |\bigcup A_i| = \sum |A_i| - \sum |A_i \cap A_j| + \dots + (-1)^{k-1}\sum |\bigcap A_{i_k}|
$$

^ Формула включения исключения
_TODO: проверить_
---

> $A \sqcup B \implies A \cup B = \emptyset; A \sqcap B = A \cap B$

---
