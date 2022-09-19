---
id: 600fgnayut4rm69k2wpemzd
title: Функция (отображение)
desc: ''
updated: 1663618828478
created: 1663227151799
---

Функция $f$ из множества $A$ в множество $B$ ($f : A \to B$) - это:
> Правило, сопоставляющее каждому элементу $a \in A$ некотрый однозначно определённый элемент $b \in B$, который называется образом элемента $a$ при отображении $f$ и обозначается $f(a); \forall a \in A \, \exists! b \in B : f(a) = b$

## Примеры
1. школьные функции: $A=B=\R$, правило - формула, напр. $f(x) = x^2-2x+3$
2. $A=[0, +\infty], \, B=\R$, правило $f(x)=\sqrt x$
3. $A - \text{люди в аудитории},\, B=\N,\, f(x) = \text{рост } x$
4. $A - \text{множество студентов},\, B - \text{множество групп},\, f(x) = \text{в какой группе учится } x$
5. $A - \text{жители Москвы},\, B - \text{дома Москвы},\, f(x) - \text{дом, где живёт } x$
6. $А,\,B$ те же, $f(x) = \text{дом, который построил } x$ - не функция!

## График функции
График $f = \lbrace (a, f(a)) \in A \times B \rbrace$

## Свойства
### Инъективность (мономорфизм)
$f(x) = f(y) \iff x = y$  
равнозначно  
$x \neq x' \iff f(x) \neq f(x')$

### Сюръективность (эпиморфизм)
$\forall y \in Y \exists x \in X : y = f(x)$

### Биективность (взаимноднозначное соответствие)
Она же "взаимоднозначное отображение"  
$f$ инъективна $\land$ $f$ сюрьективна $\iff$ $f$ биективна  
$\forall x \exists! y : y=f(x) \\
\forall y \exists! x : f(x)=y$

#### Образ отображения
$Im\,f = \lbrace y \in Y :\,\exists x \, f(x) = y \rbrace$


## Множество всех возможных функций $\space f : X \to Y$ 
$\lbrace f : X \to Y \rbrace$ oбозначается $Y^X$

Пусть $|X|=m, |Y|=k,$ тогда:
* $|Y^X|=k^m$
* $I \subset Y -$ все инъективные функции
    $$\begin{cases}
    k < m \implies |I|=0 \\
    k \geq m \implies |I|=A_k^m = k! / (k-m)!
    \end{cases}$$
* $S \subset Y -$ все сюръективные функции
    $$\begin{cases}
    m < k \implies |S|=0 \\
    m \geq k \implies ? \text{ "формула сложная, напишем потом"}
    \end{cases}$$
* $B \subset Y -$ все биективные функции
    $$\begin{cases}
    k \neq m \implies |B|=0 \\
    k = m \implies |B|=A_k^k = P_k = k!
    \end{cases}$$

## Композиция функций
Пусть $f : X \to Y, g : Y \to Z$  
$x \leadsto g(f(x)) -$ композиция $f$ и $g$  
$g \circ f : X \to Z$

### Свойства
* коммутативности в общем случае нет
* ассоциативность: $(h \circ g) \circ f = h \circ (g \circ f)$
    * $((h \circ g) \circ f)(x) = (h \circ g)(f(x)) = h(g(f(x)))$
    * $(h \circ (g \circ f))(x) = h((g \circ f)(x)) = h(g(f(x)))$
#### Tождественная функция (identity)
$Id_Y \circ f = f, f \circ Id_X = f$  
$Id_X : X \to X, Id(x) = x$

Если $f : X \to X,$ то $Id_X \circ f = f \circ Id_X = f$

#### Обратная функция
Можно ли найти такую $g : Y \to X$, что:
* $g \circ f = Id_X -$ левая обратная функция для $f$
* $f \circ h = Id_Y -$ правая обратная функция для $f$

> Теорема. $f : X \to Y$
1. у $f$ есть правая обратная функция $\iff f$ сюръективна
2. y $f$ есть левая обратная функция $\iff f$ инъективна  
*TODO*

> Следствие. $f$ биективна $\implies$ у $f$ есть "настоящая" обратная функция, т. е. $g : Y \to X$, такое, что:
* $f \circ g = Id_Y$
* $g \circ f = Id_X$
>
> Тогда $g$ обозначается $f^{-1}$

### Примеры
* вектор $\overline a$ задаёт движение плоскости $T_{\overline a} : П \to П$  
    $T_{\overline b} \circ T_{\overline a} = T_{\overline a + \overline b}$

---
> Множество биекций $f : X \to X$ обозначается $S(X)$ и называется множеством перестановок