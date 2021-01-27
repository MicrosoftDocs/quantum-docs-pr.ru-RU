---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA
title: Операция Апплиреверседопбеа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 1759764947cdbd84a1db945296d441a13f13767e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843585"
---
# <a name="applyreversedopbea-operation"></a>Операция Апплиреверседопбеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.

```qsharp
operation ApplyReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit--is-adj"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Операция, которая работает с регистром с обратным порядком байтов.


### <a name="register--littleendian"></a>Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр с прямым порядком байтов для преобразования.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбе](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [Microsoft. тактов. арифметик. Апплиреверседопбек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [Microsoft. тактов. арифметик. Апплиреверседопбека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)