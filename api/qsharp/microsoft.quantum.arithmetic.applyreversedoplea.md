---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA
title: Операция Апплиреверседоплеа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 572841410f16085256fdee9302038cd347476dd9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843529"
---
# <a name="applyreversedoplea-operation"></a>Операция Апплиреверседоплеа

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.

```qsharp
operation ApplyReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--littleendian--unit--is-adj"></a>Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода

Операция, которая работает с регистром с прямым порядком следования.


### <a name="register--bigendian"></a>Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр с обратным порядком байтов для преобразования.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Апплиреверседопле](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [Microsoft. тактов. арифметик. Апплиреверседоплек](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [Microsoft. тактов. арифметик. Апплиреверседоплека](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)