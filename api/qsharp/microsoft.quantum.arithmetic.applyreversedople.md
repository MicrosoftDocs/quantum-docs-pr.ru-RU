---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: Операция Апплиреверседопле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 16ce6842cdef8e519a13a45640edc3d79cdbce25
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202759"
---
# <a name="applyreversedople-operation"></a>Операция Апплиреверседопле

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit"></a>Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Операция, которая работает с регистром с прямым порядком следования.


### <a name="register--bigendian"></a>Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр с обратным порядком байтов для преобразования.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседоплеа](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [Microsoft. тактов. арифметик. Апплиреверседоплек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [Microsoft. тактов. арифметик. Апплиреверседоплека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)