---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730352"
---
# <a name="drawmany-operation"></a>Операция Дравмани

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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