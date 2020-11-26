---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Операция Репеатка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205411"
---
# <a name="repeatca-operation"></a>Операция Репеатка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Повторяет операцию заданное число раз.

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--tinput--unit--is-adj--ctl"></a>Op: ' Тинпут =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которая вызывается повторно.


### <a name="ntimes--int"></a>Нтимес: [int](xref:microsoft.quantum.lang-ref.int)

Число вызовов `op` .


### <a name="input--tinput"></a>входные данные: ' Тинпут

Входные данные, передаваемые в `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Дравмани](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. тактов. Canon. Репеатк](xref:Microsoft.Quantum.Canon.RepeatC)