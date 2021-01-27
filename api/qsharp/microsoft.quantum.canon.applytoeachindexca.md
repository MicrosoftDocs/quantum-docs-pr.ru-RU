---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Операция Апплитоеачиндекска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: 5046edc54576420bd8919ca52947076aed17cbce
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850799"
---
# <a name="applytoeachindexca-operation"></a>Операция Апплитоеачиндекска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому индексированному элементу в регистре.
Модификатор `CA` указывает, что операция с одним кубитом является аджоинтабле и управляемой.

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a>Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, применяемая к каждому кубит.


### <a name="register--t"></a>Register: не []

Массив Кубитс, для которого применяется заданная операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором действует каждая из операций.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоеачиндекс](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)