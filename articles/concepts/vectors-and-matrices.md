---
Title: векторы и матрицы в описании тактовых вычислений: Изучите основы работы с векторами и матрицами.
Автор: Куантумвритер UID: Microsoft. тактов. Основные понятия. Vectors MS. author: nawiebe@microsoft.com MS. Дата: 12/11/2017 MS. Topic: статья No-Loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="vectors-and-matrices"></a>Векторы и матрицы

Некоторые навыки работы с векторами и матрицами необходимы для понимания тактовых вычислений. Мы предоставляем краткое введение ниже, и заинтересованные читатели рекомендуют читать стандартную ссылку на линейную перерезку *, например Странг, G. (1993). Введение в линейную перерезку (Vol. 3). Веллеслэй, MA: Веллеслэй-Кембриджского нажмите* или онлайновую ссылку, например [линейную перерезку](http://joshua.smcvt.edu/linearalgebra/).

Вектор столбца (или просто [*вектор*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ $ версии измерения (или размера) $ n $ представляет собой набор из $ n $ комплексных чисел $ (v_1, v_2, \лдотс, v_n), $ упорядоченных в виде столбца.

$$v =\begin{bmatrix}
v_1\\\\
v_2\\\\
\вдотс\\\\
v_n\end{bmatrix}$$

Норма вектора $ v $ определяется как $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $ . Говорят, что вектор является нормой единицы (или же он называется [*вектором*](https://en.wikipedia.org/wiki/Unit_vector)), если его значение равно $ 1 $ . [*Смежная часть вектора*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ обозначается $ v ^ \dagger $ и определяется как следующий вектор строки $ \* $ , где обозначает комплексно сопряженный,

$$\begin{bmatrix}v_1 \\\\ \вдотс \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ * & \cdots & v_n ^ *\end{bmatrix}$$

Наиболее распространенным способом умножения двух векторов является [*внутренний продукт*](https://en.wikipedia.org/wiki/Inner_product_space), который также называется «точкой».  Внутренний продукт предоставляет проекцию одного вектора на другой и не имеет ценности в описании того, как выразить один вектор как сумму других простых векторов.  Внутренний продукт между $ u $ и $ v $ , обозначенным $ \left \langle u, v, \right \rangle $ определяется как

$$
\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

Эта нотация также позволяет записать норму вектора $ v $ как $ \sqrt { \langle v, v \rangle } $ .

Можно умножить вектор на число $ c, $ чтобы сформировать новый вектор, записи которого умножаются на $ c $ . Можно также добавить два вектора $ u $ и v $ , $ чтобы сформировать новый вектор, записи которого являются суммой записей $ u $ и $ v $ . Эти операции показаны ниже.

$$\mathrm{Если } ~ u=\begin{bmatrix}
u_1\\\\
u_2\\\\
\вдотс\\\\
u_n \end{bmatrix} ~ \mathrm { и}~
3,3=\begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \вдотс\\\\
    v_n \end{bmatrix} , ~ \mathrm { затем}~
Au + BV=\begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\вдотс\\\\
au_n + bv_n \end{bmatrix} .
$$

[*Матрица*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) размером $ m \times n $ представляет собой коллекцию $ $ комплексных чисел MN, упорядоченных в $ m $ строках и $ n $ столбцов, как показано ниже:

$$Пн= 
\begin{bmatrix}
M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2N}\\\\
\ddots\\\\
M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}\\\\
\end{bmatrix}.$$

Обратите внимание, что вектор измерения $ n $ — это просто матрица размера $ n \times 1 $ . Как и в случае с векторами, можно умножить матрицу на число $ c $ , чтобы получить новую матрицу, в которой каждая запись умножается на $ c $ , и мы можем добавить две матрицы одного размера, чтобы создать новую матрицу, записи которой являются суммой соответствующих записей двух матриц. 

## <a name="matrix-multiplication-and-tensor-products"></a>Умножение и продукты тензорные

Можно также умножить две матрицы $ m $ $ на Dimension m \times $ и $ n $ измерения $ n p, \times $ чтобы получить новую матрицу $ p $ измерения $ m \times p $ , как показано ниже:

\begin{align}
&\begin{bmatrix}
    M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
    M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2N}\\\\
    \ddots\\\\
    M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}
\end{bmatrix}
\begin{bmatrix}
N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1p}\\\\
N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\
\ddots\\\\
N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}
\end{bmatrix}=\begin{bmatrix}
P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1p}\\\\
P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\
\ddots\\\\
P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}
\end{bmatrix}
\end{align}

где записи $ P $ — $ P_ { ОК } = \sum _j M_ { ИЖ } N_ { ЖК } $ . Например, запись $ P_ { 11 } $ — это внутреннее произведение первой строки $ M $ с первым столбцом $ N $ . Обратите внимание, что поскольку вектор является просто особым случаем матрицы, это определение расширяется на умножение векторных матриц. 

Все матрицы, которые мы будем рассматривать, представляют собой квадратные матрицы, где число строк и столбцов равно, или векторы, которые соответствуют только $ одному $ столбцу. Одна особая квадратная матрица — это [*единичная матрица*](https://en.wikipedia.org/wiki/Identity_matrix), помеченная $ \boldone $ , в которой все его диагональные элементы равны $ 1 $ , а остальные элементы равны $ 0 $ :

$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\\\
0 ~~ 1 ~~ \cdots ~~ 0\\\\
~~ \ddots\\\\
0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$

Для квадратной матрицы $ a $ мы говорим, что матрица $ B $ является [*обратной*](https://en.wikipedia.org/wiki/Invertible_matrix) , если $ AB = Ба = \boldone $ . Обратная часть матрицы не должна существовать, но, если она существует, она уникальна и обстоится $ как ^ { -1 } $ . 

Для любой матрицы $ m $ прилегающий или сопряженный с $ m $ является матрицей $ N $ , такой, что $ N_ { ИЖ } = M_ { ji } ^ \* $ . Смежная часть $ M $ обычно обозначается как $ m ^ \dagger $ . Мы говорим, что матрица $ U $ является [*единой*](https://en.wikipedia.org/wiki/Unitary_matrix) $ , если УУ ^ u \dagger = ^ \dagger u = \boldone $ или аналогичным, $ u ^ { -1 } = u ^ \dagger $ .  Возможно, наиболее важным свойством единой матрицы является то, что они сохраняют норму вектора.  Это происходит из-за того, что 

$$\langlev, v v \rangle = ^ \dagger v ^ = u ^ \dagger { -1 } U v = v ^ \dagger u ^ u v \dagger = \langle , u v \rangle .$$  

Матрица $ m $ называется [*хермитиан*](https://en.wikipedia.org/wiki/Hermitian_matrix) , если $ m = m ^ \dagger $ .

Наконец, [*продукт тензорные*](https://en.wikipedia.org/wiki/Tensor_product) (или кронеккер продукт) двух матриц $ M $ размером $ m \times n $ и $ n $ из размера $ p \times q $ — это более крупная матрица $ p = M n с \otimes $ размером $ MP \times НК $ , и она получается из $ M $ и $ n $ следующим образом:

\begin{align}
    M \otimes N&=
    \begin{bmatrix}
        M_ { 11 } ~~ \cdots ~~ M_ { 1N }\\\\
        \ddots\\\\
        M_ { M1 } ~~ \cdots ~~ M_ { MN  }
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\
        \ddots\\\\
        N_ { P1 } ~~ \cdots ~~ N_ { PQ}
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}\\\\
        \ddots\\\\
        M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { MN } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}
    \end{bmatrix}.
\end{align}

Это лучше продемонстрировать с помощью некоторых примеров:

$$
    \begin{bmatrix}
        a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ е \end{bmatrix}=
    \begin{bmatrix}
        a \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
        \\\\[1,5 EM] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
    \end{bmatrix}
    =a б a b \begin{bmatrix} \\\\ \\\\ \\\\ c \\\\ б \\\\\end{bmatrix}
$$

и

$$
    \begin{bmatrix}
        a \ b \\\\ c \ d\end{bmatrix}
    \otimes 
    \begin{bmatrix}
        e \ f \\\\ g \ h\end{bmatrix}
     =
    \begin{bmatrix}
    конкретного\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    &\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    четырехмерного\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \end{bmatrix}
    =
    \begin{bmatrix}
    AE \ AF \ BF\\\\
    AG \ AH \ BG \ BH\\\\
    CE \ CF \ de \ DF\\\\
    CG \ CH \ \end{bmatrix} , DH.
$$

Последнее полезное соглашение об обозначении, окружающее продукты тензорные, заключается в том, что для любой векторной $ v $ или матрицы $ m $ , $ v ^ { \otimes n } $ или $ m ^ { \otimes n } $ это короткий рукой для $ $ повторяющегося тензорные продукта n.  Пример:

\begin{align}
&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1-1 \\\\ \\\\ 1 \end{bmatrix} ,\\\\
  &\begin{bmatrix}0 1 1 0 1 0 1 1 0 & \\\\ & \end{bmatrix} ^ { \otimes } = \begin{bmatrix} & \\\\ & \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & & & \\\\ & & & \\\\ & & & \\\\ & & & \end{bmatrix} 0 0 1 0 0 1 0 0 1 0 0 1 0 0.
\end{align}
