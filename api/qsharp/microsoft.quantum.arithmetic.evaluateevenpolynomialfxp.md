---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Операция Евалуативенполиномиалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: c3129cb796a344f7ad38a585183db285d48892bf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843231"
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

