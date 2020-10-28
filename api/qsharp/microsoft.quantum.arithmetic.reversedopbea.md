---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: Функция Реверседопбеа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: b2418911e71c0b98e1a78247b2ae066887d89cd8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730568"
---
# <a name="reversedopbea-function"></a>Функция Реверседопбеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit-adj"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit-adj"></a>Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбе](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбек](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [Microsoft. тактов. арифметик. Реверседопбека](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)