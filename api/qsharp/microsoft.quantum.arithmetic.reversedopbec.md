---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: Функция Реверседопбек
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5e9aa6e6dfef74bca004170cf2b1cd91aa13f0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730553"
---
# <a name="reversedopbec-function"></a>Функция Реверседопбек

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit-ctl"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit-ctl"></a>Выходные данные [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => CTL [единицы](xref:microsoft.quantum.lang-ref.unit) литтлиндиан

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [Microsoft. тактов. арифметик. Реверседопбе](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбека](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)