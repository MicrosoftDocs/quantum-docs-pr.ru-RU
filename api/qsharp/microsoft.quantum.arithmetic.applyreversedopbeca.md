---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Операция Апплиреверседопбека
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 5c761fb8e1042a25cd2e88f1b33e597c7d9287f9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202725"
---
# <a name="applyreversedopbeca-operation"></a>Операция Апплиреверседопбека

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit--is-adj--ctl"></a>Op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"

Операция, которая работает с регистром с обратным порядком байтов.


### <a name="register--littleendian"></a>Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр с прямым порядком байтов для преобразования.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбе](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [Microsoft. тактов. арифметик. Апплиреверседопбеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. тактов. арифметик. Апплиреверседопбек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)