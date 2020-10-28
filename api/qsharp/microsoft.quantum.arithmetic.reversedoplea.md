---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: Функция Реверседоплеа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: eabeb8e068ef32cf6717efd6e818271a667b39b2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730529"
---
# <a name="reversedoplea-function"></a>Функция Реверседоплеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit-adj"></a>Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)

Операция, входные данные которой должны быть отменены.



## <a name="output--bigendian--unit-adj"></a>Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)

Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [Microsoft. тактов. арифметик. Реверседопле](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. тактов. арифметик. Реверседоплек](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [Microsoft. тактов. арифметик. Реверседоплека](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)