---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210001"
---
# <a name="drawmany-operation"></a>Операция Дравмани

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Повторяет операцию для заданного числа выборок, собирая выходные данные в массиве.

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a>Входные данные

### <a name="op--tinput--toutput"></a>Op: ' Тинпут => ' Таутпут 

Операция, которая вызывается повторно.


### <a name="nsamples--int"></a>Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)

Число выборок вызова `op` для сбора.


### <a name="input--tinput"></a>входные данные: ' Тинпут

Входные данные, передаваемые в `op` .



## <a name="output--toutput"></a>Выходные данные: ' Таутпут []



## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут


### <a name="toutput"></a>' Таутпут



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.Repeat)