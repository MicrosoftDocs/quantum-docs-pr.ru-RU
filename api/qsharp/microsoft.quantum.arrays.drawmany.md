---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846210"
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



## <a name="example"></a>Пример

Следующий пример кода выдает целое число с учетом операции, которая производит выборку по одному биту за раз.

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. REPEAT](xref:Microsoft.Quantum.Canon.Repeat)