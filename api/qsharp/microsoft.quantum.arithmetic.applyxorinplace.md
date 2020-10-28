---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Операция Аппликсоринплаце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 5a35abc16a967e64c84466a47844ed7beeb618dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731697"
---
# <a name="applyxorinplace-operation"></a>Операция Аппликсоринплаце

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Применяет операцию побитового исключающего XOR между классическим целым числом и целым числом, представленным регистром Кубитс.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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

