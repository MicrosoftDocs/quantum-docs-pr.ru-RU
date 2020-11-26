---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Операция Скуареи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 79a431d411c4ffd502fb5338b5396341fd63aea8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221867"
---
# <a name="squarei-operation"></a>Операция Скуареи

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Вычисляет квадрат целого числа `xs` в `result` , который должен быть равен нулю изначально.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-разрядное число в квадрат (Литтлиндиан)


### <a name="result--littleendian"></a>результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2N $-bit Result (Литтлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Использует стандартный подход Shift и-Add для расчета квадрата. Сохраняет $n-$1 Кубитс по сравнению с прямым решением, которое сначала копирует XS перед применением обычного множителя, а затем отменяет операцию копирования.