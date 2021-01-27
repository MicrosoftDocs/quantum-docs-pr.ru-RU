---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Операция КомпутереЦипрокалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: db7425f1a8a9b5ddfdc6b123dad003298e3670e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843244"
---
# <a name="computereciprocalfxp-operation"></a>Операция КомпутереЦипрокалфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Вычисление $1/x $ для числа с фиксированной запятой $x $.

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="x--fixedpoint"></a>x: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Число с фиксированной запятой, которое необходимо инвертировать.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Число с фиксированной запятой, которое будет содержать результат. Необходимо инициализировать в $ \ket{0.0} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

