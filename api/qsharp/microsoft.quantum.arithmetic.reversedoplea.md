---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: Функция Реверседоплеа
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 71b6b87a44f541e5379d8de8a3562febbfa49e1d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222173"
---
# <a name="reversedoplea-function"></a>Функция Реверседоплеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit--is-adj"></a>Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Операция, входные данные которой должны быть отменены.



## <a name="output--bigendian--unit--is-adj"></a>Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [Microsoft. тактов. арифметик. Реверседопле](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. тактов. арифметик. Реверседоплек](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [Microsoft. тактов. арифметик. Реверседоплека](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)