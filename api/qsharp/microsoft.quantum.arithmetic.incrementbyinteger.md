---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Операция Инкрементбинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 363d48d697e3b2dad4d4896e6b1e701864649d9b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731512"
---
# <a name="incrementbyinteger-operation"></a>Операция Инкрементбинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Увеличивает значение регистра неподписанного такта на классическое целое число с использованием ротаций фазы.

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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

