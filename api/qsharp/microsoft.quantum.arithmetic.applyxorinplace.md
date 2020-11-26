---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Операция Аппликсоринплаце
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210119"
---
# <a name="applyxorinplace-operation"></a>Операция Аппликсоринплаце

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию побитового исключающего XOR между классическим целым числом и целым числом, представленным регистром Кубитс.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Применяет `X` операции к Кубитс в регистре с прямым порядком следования на основе 1 битов в целом.

Давайте обстоится в `value` , а y — это целое число без знака, закодированное в `target` , а затем `InPlaceXorLE` выполняет операцию, указанную в следующем сопоставлении: $ \кет{и}\ригхтарров \кет{и\оплус a} $, где $ \оплус $ является побитовым ИСКЛЮЧАЮЩИМ оператором или.

## <a name="input"></a>Входные данные

### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленное значение, которое считается неотрицательным.


### <a name="target--littleendian"></a>Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта, который используется для хранения `value` в кодировке с прямым порядком байтов.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

