---
uid: Microsoft.Quantum.Canon.NoOp
title: Операция NoOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 45f3c8c9d4bae8ac8f7f60c4e4f8ead5d92e7c00
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852388"
---
# <a name="noop-operation"></a>Операция NoOp

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Выполняет операцию идентификации (No-op) для аргумента.

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
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