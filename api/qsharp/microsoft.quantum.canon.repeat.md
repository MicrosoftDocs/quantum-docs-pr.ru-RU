---
uid: Microsoft.Quantum.Canon.Repeat
title: Повторить операцию
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715594"
---
# <a name="repeat-operation"></a>Повторить операцию

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Повторяет операцию заданное число раз.

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--tinput--unit"></a>Op: "Тинпут = [единица](xref:microsoft.quantum.lang-ref.unit)> 

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
- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. тактов. Canon. Репеатк](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. тактов. Canon. Репеатка](xref:Microsoft.Quantum.Canon.RepeatCA)