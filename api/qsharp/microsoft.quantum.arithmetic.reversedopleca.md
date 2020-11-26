---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Функция Реверседоплека
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: c058243db2b4cee3a72e025b084b4f98f7020a6b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222071"
---
# <a name="reversedopleca-function"></a>Функция Реверседоплека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit--is-adj--ctl"></a>Op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Операция, входные данные которой должны быть отменены.



## <a name="output--bigendian--unit--is-adj--ctl"></a>Выходные данные [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"

Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [Microsoft. тактов. арифметик. Реверседопле](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. тактов. арифметик. Реверседоплеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. тактов. арифметик. Реверседоплек](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)