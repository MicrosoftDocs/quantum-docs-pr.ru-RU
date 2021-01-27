---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Операция Апплитоеача
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844604"
---
# <a name="applytoeacha-operation"></a>Операция Апплитоеача

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому элементу в регистре.
Модификатор `A` указывает, что единственной операцией кубит является аджоинтабле.

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--t--unit--is-adj"></a>Синглилементоператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

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

- [Microsoft. тактов. Canon. Апплитоеач](xref:Microsoft.Quantum.Canon.ApplyToEach)