---
uid: Microsoft.Quantum.Canon.Repeat
title: Повторить операцию
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: cd572e5e082df94d762a0869ad2c1923fb71fd3d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205608"
---
# <a name="repeat-operation"></a>Повторить операцию

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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