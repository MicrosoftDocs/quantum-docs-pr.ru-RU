---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Операция Евалуатеоддполиномиалфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: d52da4092f16d43ab9d08b03f798a4d6789c7348
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731568"
---
# <a name="evaluateoddpolynomialfxp-operation"></a>Операция Евалуатеоддполиномиалфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Вычисляет нечетный полином в представлении с фиксированной запятой.

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты нечетнымго полинома в виде двойного массива, т. е. массива $ [a_0, a_1,..., a_k] $ для нечетного $P (x) = a_0 x + a_1 x ^ 3 + \кдотс + a_k x ^ {2000 + 1} $.


### <a name="fpx--fixedpoint"></a>ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Входное число с фиксированной запятой, для которого вычисляется степень полинома.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Выходное число с фиксированной запятой, которое будет содержать P (x). Должно быть в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

