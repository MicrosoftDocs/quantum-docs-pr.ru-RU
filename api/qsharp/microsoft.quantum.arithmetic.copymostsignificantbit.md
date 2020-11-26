---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Операция Копимостсигнификантбит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 39a2dc2fe33f46c2767def06a44cde07e2f01497
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223295"
---
# <a name="copymostsignificantbit-operation"></a>Операция Копимостсигнификантбит

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Копирует наиболее значащий бит регистра кубит `from` , представляющий целое число без знака, в кубит `target` .

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="from--littleendian"></a>с: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Целое число без знака, из которого копируется наибольший бит.
целое число кодируется в формате с прямым порядком байтов.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, в котором копируется наибольший бит. Битовая кодировка определяется на основе вычислений.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. арифметик. Литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)