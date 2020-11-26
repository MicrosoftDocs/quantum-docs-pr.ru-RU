---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Операция Мултиплифксп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 3c9ef9ade660e1f420d85162104d773b96722eeb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222615"
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



## <a name="remarks"></a>Комментарии

Текущая реализация требует, чтобы три цифры с фиксированной запятой имели одинаковую позицию и одно и то же число Кубитс.