---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Операция Апплитоеачка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841487"
---
# <a name="applytoeachca-operation"></a>Операция Апплитоеачка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому элементу в регистре.
Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a>Синглилементоператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

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