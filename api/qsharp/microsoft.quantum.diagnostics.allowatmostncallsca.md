---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Операция Алловатмостнкаллска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202572"
---
# <a name="allowatmostncallsca-operation"></a>Операция Алловатмостнкаллска

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Между вызовом этой операции и ее прилегающим объектом утверждается, что данная операция вызывается не чаще определенного числа раз.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="ntimes--int"></a>Нтимес: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное число вызовов, которое `op` может быть вызвано.


### <a name="op--tinput--toutput--is-adj--ctl"></a>Op: "Тинпут =>" Таутпут — "года + CTL"

Операция, вызовы которой должны быть ограничены.


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Сообщение, отображаемое при сбое.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут


### <a name="toutput"></a>' Таутпут



## <a name="remarks"></a>Комментарии

Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.