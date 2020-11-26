---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: Функция Реверседопбека
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: da21b09110400ad4ee862f662d45e166a49e7bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222207"
---
# <a name="reversedopbeca-function"></a>Функция Реверседопбека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit--is-adj--ctl"></a>Op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Выходные данные [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [Microsoft. тактов. арифметик. Реверседопбе](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбек](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)