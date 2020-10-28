---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Функция Куантумром
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 8ba5c6fab4abcfaee7233df9535f22eea5f68c28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732624"
---
# <a name="quantumrom-function"></a>Функция Куантумром

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакеты [](https://nuget.org/packages/)


Использует методику такта для представления заданной матрицы плотности.

Учитывая список коэффициентов $N $ alpha_j $, он возвращает единую $U $, которая использует методику такта для подготовки приближения $ \тилде\рхо\ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} $ пурификатион матрицы плотности $ \рхо = \ sum_ {j = 0} ^ {N-1} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $. В этом приближении ошибка $ \епсилон $ заключается в том, что $ | p_j-\фрак{| alpha_j |} {\ sum_k | \ alpha_k |} | \ле \епсилон/N $ and $ \| \тилде\рхо-\рхо \| \ле \епсилон $. Иными словами, $ $ \бегин{алигн} У\кет {0} ^ {\лцеил\ Log_2 н\рцеил} \ Сисакет {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}.
\енд{алигн} $ $

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a>Входные данные

### <a name="targeterror--double"></a>Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)

Целевая ошибка $ \епсилон $.


### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив коэффициентов $N $ с указанием вероятности базисных состояний.
Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.



## <a name="output--intintintdoublelittleendianqubit--unit-adj--ctl"></a>Выходные данные: ([(int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))[, Double](xref:microsoft.quantum.lang-ref.double), ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) Нагода + CTL)

## <a name="first-parameter"></a>Первый параметр

Кортеж, `(x,(y,z))` где `x = y + z` — Общее число выделенных Кубитс, `y` — число Кубитс для `LittleEndian` регистра, а `z` — число Кубитс мусора.

## <a name="second-parameter"></a>Второй параметр

Один из норм $ \ sum_j | \ alpha_j | $ массива коэффициента.

## <a name="third-parameter"></a>Третий параметр

Единая $U $.

## <a name="references"></a>Ссылки

- Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662