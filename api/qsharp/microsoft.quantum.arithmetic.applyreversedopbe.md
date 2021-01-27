---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBE
title: Операция Апплиреверседопбе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBE
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: bf2d43d4e870150f8e6d51dc2f5fb37bdf01d6ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843614"
---
# <a name="applyreversedopbe-operation"></a>Операция Апплиреверседопбе

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.

```qsharp
operation ApplyReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--bigendian--unit"></a>Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Операция, которая работает с регистром с обратным порядком байтов.


### <a name="register--littleendian"></a>Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр с прямым порядком байтов для преобразования.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопбеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. тактов. арифметик. Апплиреверседопбек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [Microsoft. тактов. арифметик. Апплиреверседопбека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)