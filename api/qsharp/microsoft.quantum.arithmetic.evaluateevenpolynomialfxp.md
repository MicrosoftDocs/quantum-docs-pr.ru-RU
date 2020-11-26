---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Операция Евалуативенполиномиалфксп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: 21c700ccb2b87b906fc4d8b65eddf962353948c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223261"
---
# <a name="evaluateevenpolynomialfxp-operation"></a>Операция Евалуативенполиномиалфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Вычисляет четность в представлении с фиксированной запятой.

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты равномерности в виде массива типа Double, т. е. массива $ [a_0, a_1,..., a_k] $ для четного $P (x) = a_0 + a_1 x ^ 2 + \кдотс + a_k x ^ {2000} $.


### <a name="fpx--fixedpoint"></a>ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Входное число с фиксированной запятой, для которого вычисляется степень полинома.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Выходное число с фиксированной запятой, которое будет содержать $P (x) $. Должно быть в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

