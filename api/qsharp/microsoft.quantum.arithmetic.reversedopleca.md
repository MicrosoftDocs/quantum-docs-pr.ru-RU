---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Функция Реверседоплека
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d4245437f2b71abb8bf1bbe4db43ae7d2ee23799
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845757"
---
# <a name="reversedopleca-function"></a>Функция Реверседоплека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit--is-adj--ctl"></a>Op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Операция, входные данные которой должны быть отменены.



## <a name="output--bigendian--unit--is-adj--ctl"></a>Выходные данные [](xref:Microsoft.Quantum.Arithmetic.BigEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"

Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [Microsoft. тактов. арифметик. Реверседопле](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. тактов. арифметик. Реверседоплеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. тактов. арифметик. Реверседоплек](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)