---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Операция Апплитоеачиндекска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208947"
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