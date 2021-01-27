---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Операция Копимостсигнификантбит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843269"
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