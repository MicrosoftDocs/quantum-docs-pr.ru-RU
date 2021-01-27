---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Операция Мултиплиси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7c7e7dfaee9b9dc717db44956506984e60281dd2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843019"
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

