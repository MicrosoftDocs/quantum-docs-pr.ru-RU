---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Функция Реверседоплека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b5413e43ad50ba7252705ef53b21e63650dbb2a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730513"
---
# <a name="reversedopleca-function"></a>Функция Реверседоплека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit-adj--ctl"></a>Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Операция, входные данные которой должны быть отменены.



## <a name="output--bigendian--unit-adj--ctl"></a>Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [Microsoft. тактов. арифметик. Реверседопле](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. тактов. арифметик. Реверседоплеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. тактов. арифметик. Реверседоплек](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)