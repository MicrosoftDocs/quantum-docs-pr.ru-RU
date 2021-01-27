---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Операция Аппликсоринплаце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 8f338d6638d554f3ead1f3c0e7b6605c7937abd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843470"
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

