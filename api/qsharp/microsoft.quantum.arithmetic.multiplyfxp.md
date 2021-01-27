---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Операция Мултиплифксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 776ccb7a9e1ba1a34b28da6e1cf3a0aafe9da76b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843051"
---
# <a name="multiplyfxp-operation"></a>Операция Мултиплифксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Умножает два числа с фиксированной запятой в тактовые регистры.

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="fp1--fixedpoint"></a>FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Первое число с фиксированной запятой.


### <a name="fp2--fixedpoint"></a>Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Второе число с фиксированной запятой.


### <a name="result--fixedpoint"></a>результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Число с фиксированной запятой результата должно быть в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Текущая реализация требует, чтобы три цифры с фиксированной запятой имели одинаковую позицию и одно и то же число Кубитс.