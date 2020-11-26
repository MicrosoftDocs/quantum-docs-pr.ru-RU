---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Операция Апплитоеач
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217872"
---
# <a name="applytoeach-operation"></a>Операция Апплитоеач

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому элементу в регистре.

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--t--unit"></a>Синглилементоператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, применяемая к каждому кубит.


### <a name="register--t"></a>Register: не []

Массив Кубитс, для которого применяется заданная операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором действует операция.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоеачк](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [Microsoft. тактов. Canon. Апплитоеача](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [Microsoft. тактов. Canon. Апплитоеачка](xref:Microsoft.Quantum.Canon.ApplyToEachCA)