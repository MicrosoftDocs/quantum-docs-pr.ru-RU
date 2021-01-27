---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Операция Евалуатеоддполиномиалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 852e986cd09c3b2e31263f53e381d9da73298415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846669"
---
# <a name="evaluateoddpolynomialfxp-operation"></a>Операция Евалуатеоддполиномиалфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Вычисляет нечетный полином в представлении с фиксированной запятой.

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты нечетнымго полинома в виде двойного массива, т. е. массива $ [a_0, a_1,..., a_k] $ для нечетного $P (x) = a_0 x + a_1 x ^ 3 + \кдотс + a_k x ^ {2000 + 1} $.


### <a name="fpx--fixedpoint"></a>ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Входное число с фиксированной запятой, для которого вычисляется степень полинома.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Выходное число с фиксированной запятой, которое будет содержать P (x). Должно быть в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

