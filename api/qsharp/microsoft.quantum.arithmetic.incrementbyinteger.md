---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Операция Инкрементбинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222972"
---
# <a name="incrementbyinteger-operation"></a>Операция Инкрементбинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Увеличивает значение регистра неподписанного такта на классическое целое число с использованием ротаций фазы.

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Предположим, что `target` кодирует целое число без знака $x $ в кодировке с прямым порядком байтов и `increment` равно $a $.
Затем эта операция реализует единую $ \кет{КС} \мапсто \кет{КС + a} $, где сложение выполняется по модулю $2 ^ n $, где $n = \Тексттт{ленгс (Target!)} $.

## <a name="input"></a>Входные данные

### <a name="increment--int"></a>приращение: [int](xref:microsoft.quantum.lang-ref.int)

Целое число, на которое `target` увеличивается значение.


### <a name="target--littleendian"></a>Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Тактовый регистр кодирует целое число без знака, используя обратную кодировку с прямым порядком байтов.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

