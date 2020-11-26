---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Операция Евалуатеполиномиалфксп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 4f6ed4b34af2e63dd8ee31fb9b93119e06e3ecbc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223193"
---
# <a name="evaluatepolynomialfxp-operation"></a>Операция Евалуатеполиномиалфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Вычисляет значение полинома в представлении с фиксированной запятой.

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты полинома в виде массива Double, т. е. массива $ [a_0, a_1,..., a_d] $ для полиномного $P (x) = a_0 + a_1 x + \кдотс + a_d x ^ d $.


### <a name="fpx--fixedpoint"></a>ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Входное число с фиксированной запятой, для которого вычисляется степень полинома.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Выходное число с фиксированной запятой, которое будет содержать $P (x) $. Должно быть в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

