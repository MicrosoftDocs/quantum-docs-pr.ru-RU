---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Операция Апплитоеач
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 61dda69751989ef8a98fa8fb01d832014ec4ad35
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844626"
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

## <a name="example"></a>Пример

Подготовьте три-кубит $ \кет{+} $ State:

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоеачк](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [Microsoft. тактов. Canon. Апплитоеача](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [Microsoft. тактов. Canon. Апплитоеачка](xref:Microsoft.Quantum.Canon.ApplyToEachCA)