---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Операция Апплитоеачиндекс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 746bc19f7a137ef476a25abdabc4737ed6727ff2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217619"
---
# <a name="applytoeachindex-operation"></a>Операция Апплитоеачиндекс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому индексированному элементу в регистре.

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--intt--unit"></a>Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), t) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, применяемая к каждому кубит.


### <a name="register--t"></a>Register: не []

Массив Кубитс, для которого применяется заданная операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором действует каждая из операций.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоеач](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [Microsoft. тактов. Canon. Апплитоеачиндекса](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [Microsoft. тактов. Canon. Апплитоеачиндекск](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [Microsoft. тактов. Canon. Апплитоеачиндекска](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)