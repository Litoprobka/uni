---
id: x3ke20lnysm62c3ytstrwxm
title: Множества
desc: ""
updated: 1666275561533
created: 1662203709500
---

## Определения множества

- Множество - набор элементов без определённого порядка
- Множеством называется любая совокупность объектов реального мира, мыслимая как единое целое

_Множество - неопределимое понятие_

## Misc

$$
\def\set#1{\lbrace #1 \rbrace}
\text{Задание множества: } \set{ 1, 3, 5, 7, 9 } = \set{ x | x=2n-1, n \in \N, x < 10 } \\
\text{Пустое множество } \empty = \set{} \\
\text{Множество со всеми возможными элементами (на самом деле нет) } \Omega = \set{x | \exists A.\ x \in A} \\
$$

## Основные числовые множества

- $\N : \lbrace 1, 2, 3 .. \rbrace$
- $\Z : \lbrace 0, 1, -1, 2, -2... \rbrace$
- $\Q : \lbrace {p \over q}, p \in \Z, q \in N \rbrace$
- $II$ - иррациональные числа
- $\R = \Q \cup II$
- $\Complex$

## Подмножество

$$
\def\set#1{\lbrace #1 \rbrace}
A \subset B \implies \forall x \in A\ (x \in B) \\
A = B \iff A \subset B \land B \subset A \\
C \subset A \land C \neq A:\, C - \text{собственное подмножество} \\
x \subset A \nLeftrightarrow x \in A \\
\set{x} \neq \set{\set{x}} \\
$$

## Операции над множествами

$$
\def\set#1{\lbrace #1 \rbrace}
\text{Дополнение } \overline A = \set{x \in U | x \notin A} \\
\overline{\overline A} = A - \text{инволютивность} \\
\text{Пересечение } A \cap B = \set{x \in U : x \in A \land x \in B} \\
\text{Объединение } A \cup B = \set{x \in U : x \in A \lor x \in B}
$$

## Законы

### Пересечение

$$
\begin{align}
A \cap B = B \cap A - \text{коммутативность} \\
A \cap B \cap C = (A \cap B) \cap C = A \cap (B \cap C) - \text{ассоциативность} \\
A \cap \Omega = A - \text{нейтральный элемент}
\end{align}
$$

Таким образом, множество множеств (bruh), $\cap$ и $\Omega$ образуют [[коммутативную группу | math.group-theory]].

### Объединение

$$
\begin{align}
A \cup B = B \cup A - \text{коммутативность} \\
A \cup B \cup C = (A \cup B) \cup C = A \cup (B \cup C) - \text{ассоциативность} \\
A \cup \empty = A - \text{нейтральный элемент}
\end{align}
$$

Множество множеств с $\cup$ и $\empty$ также образуют [[коммутативную группу | math.group-theory]].

### Дистрибутивность

$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C) - \text{дистрибутивность } \cap \text{ относительно } \cup \\
A \cup (B \cap C) = (A \cup B) \cap (A \cup C) - \text{дистрибутивность } \cup \text{ относительно } \cap \\
A \cap (B \setminus C) = (A \cap B) \setminus (A \cap C) - \text{дистрибутивность } \cap \text{ относительно } \setminus
$

### Законы Де Моргана

- $\overline{A \cup B} = \overline A \cap \overline B$

- $\overline{A \cap B} = \overline A \cup \overline B$

## Разность и симметрическая сумма

$\def\set#1{\lbrace #1 \rbrace}
A \setminus B = \set{x : x \in A \land x \notin B} \\
A \oplus B = \set{x : x \in A \cup B \land x \notin A \cap B} = \set{(A \setminus B) \cup (B \setminus A)} \\
A \oplus A = \empty \\
A \oplus \empty = A \\
A \oplus \overline A = \Omega
$

## Дополнительность

$
A \cup \overline A = \Omega \\
A \cap \overline A = \empty \\
\overline \Omega = \empty \\
\overline \empty = \Omega
$

## Поглощение

$
A \cup (A \cap B) = A \\
A \cap (A \cup B) = A
$

---

## Мощность множества

Moщность множества - количество элементов в нём; обозначается $|A|$ или $\#A$

## ???

$F = \lbrace n \in \N | \exists x, y, z.\, x^n + y^n = z^n \rbrace \\
F = \lbrace 1, 2 \rbrace \\
  \text{это доказали только через несколько столетий}$

$T = \lbrace x \in \N | x \text{ простые }, x+2 \text{ простые} \rbrace \\
T=\,?$

## Парадокс Рассела

Временное определение: множество $A$ - хорошее, если $A \notin A$

Пусть $В$ множество всех хороших множеств. $W$ - хорошее?  
$W = \lbrace X | X - \text{хорошее} \rbrace$

$W$ - хорошее $\implies W \in W \implies W -$ плохое  
$W$ - плохое $\implies W \notin W \implies W -$ хорошее

## Аксиоматика Цермело-Френкеля (ZF-аксиоматика)

Очень замороченная, так что лучше в неё не углубляться.  
Простым языком, аксиоматика ограничивает правила определения множеств так, чтобы не были возможны противоречия.

### Способы задания множеств

- [[операции над множествами | math.set#операции-над-множествами]]
- перечисление всех его элементов: $A=\lbrace a_1, a_2, a_3... \rbrace$
- задание надмножества и условия: $A=\lbrace x \in N : x < 10 \rbrace$

#### Декартово произведение

$A \times B = \lbrace (a, b) | a \in A,\, b \in B \rbrace$

##### Примеры

$$
\text{Плоскость} - \R \times \R \\
\text{Пространство} - \R \times \R \times \R \\
\text{Корпуса } K = \lbrace А, Б, В, Г, Д \rbrace \\
\text{Номер аудитории} - K \times \N \\
\text{Время} - {часы} \times {минуты}
$$

##### Кортеж

$X_1 \times X_2 \times ... \times X_n \\
= \lbrace (x_1, x_2, ... x_n) | x_i \in X_i \rbrace$

#### Множество подмножеств множества A

$\lbrace C : C \in A \rbrace$  
Обозначения:

- $\mathcal B$
- $\mathcal P$
- $2^A$

##### Примеры

$$
\def\set#1{\lbrace #1 \rbrace}
A = \set{x, y} \\
2^A = \set{\empty, \set{x}, \set{y}, A}\\
\#(2^A) = 4 \\
B = \set{x, y, z} \\
2^B = \set{\empty, \set{x}, \set{y}, \set{z}... \set{x, y, z}} \\
\#(2^B) = 8 \\
\#(2^X) = 2^{\#X}
$$
