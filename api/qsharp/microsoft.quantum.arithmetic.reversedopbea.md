---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: Функция Реверседопбеа
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 69fd4401e6862a3a6afaa51fb5b8a3592768bb42
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222309"
---
# <a name="reversedopbea-function"></a>Функция Реверседопбеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit--is-adj"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit--is-adj"></a>Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбе](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбек](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [Microsoft. тактов. арифметик. Реверседопбека](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)