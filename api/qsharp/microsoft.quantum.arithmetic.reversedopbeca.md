---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: Функция Реверседопбека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5617e191260903ac25effc8b922810932b7dc505
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730545"
---
# <a name="reversedopbeca-function"></a>Функция Реверседопбека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit-adj--ctl"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit-adj--ctl"></a>Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [Microsoft. тактов. арифметик. Реверседопбе](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбек](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)