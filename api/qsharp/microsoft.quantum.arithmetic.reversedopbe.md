---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: Функция Реверседопбе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846484"
---
# <a name="reversedopbe-function"></a>Функция Реверседопбе

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Операция, входные данные которой должны быть отменены.



## <a name="output--littleendian--unit"></a>Выходные данные [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан 

Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбе](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [Microsoft. тактов. арифметик. Реверседопбеа](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Microsoft. тактов. арифметик. Реверседопбек](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [Microsoft. тактов. арифметик. Реверседопбека](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)