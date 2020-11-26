---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Операция Апплитоеачиндекск
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 38fa23c70965118f1787f156bd617d6e967aba05
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217668"
---
# <a name="applytoeachindexc-operation"></a>Операция Апплитоеачиндекск

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну операцию кубит к каждому индексированному элементу в регистре.
Модификатор `C` указывает, что операция с одним кубит является управляемой.

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="singleelementoperation--intt--unit--is-ctl"></a>Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL

Операция, применяемая к каждому кубит.


### <a name="register--t"></a>Register: не []

Массив Кубитс, для которого применяется заданная операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором действует каждая из операций.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитоеачиндекс](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)