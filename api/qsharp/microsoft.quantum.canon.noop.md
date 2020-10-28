---
uid: Microsoft.Quantum.Canon.NoOp
title: Операция NoOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715761"
---
# <a name="noop-operation"></a>Операция NoOp

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Выполняет операцию идентификации (No-op) для аргумента.

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a>Описание

Эта операция принимает значение любого типа и не выполняет никаких действий.
Это может быть полезно, если ожидается входные данные типа операции, но никакие действия не выполняются.
Например, если определенная ошибка исправления ошибки синдром указывает на отсутствие ошибок, `NoOp<Qubit[]>` может быть правильной процедурой восстановления.
Аналогично, если в качестве входных данных для операции требуется процедура подготовки состояния, `NoOp<Qubit[]>` можно использовать для подготовки состояния $ \ket{0 \кдотс 0} $.

## <a name="input"></a>Входные данные

### <a name="input--t"></a>входные данные: 'T

Значение, которое необходимо пропускать.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Почти во всех случаях параметр типа для `NoOp` должен быть указан явным образом. Например, `NoOp<Qubit>` идентично <xref:microsoft.quantum.intrinsic.i> .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. внутренний. I](xref:Microsoft.Quantum.Intrinsic.I)