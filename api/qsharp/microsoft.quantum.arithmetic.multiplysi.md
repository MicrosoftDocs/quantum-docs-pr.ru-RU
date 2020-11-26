---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Операция Мултиплиси
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 4e7f43f88654f10ece4f9c30c5bfde9a779b18ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222445"
---
# <a name="multiplysi-operation"></a>Операция Мултиплиси

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Выполните умножение целого числа со `xs` знаком на целое число `ys` и сохраните результат в `result` , который должен быть равен нулю изначально.

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--signedlittleendian"></a>xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-разрядный множимое (Сигнедлиттлиндиан)


### <a name="ys--signedlittleendian"></a>ИС: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-разрядный множитель (Сигнедлиттлиндиан)


### <a name="result--signedlittleendian"></a>результат: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

2N-разрядный результат (Сигнедлиттлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

