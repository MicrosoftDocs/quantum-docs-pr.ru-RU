---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Функция Нмисклассификатионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709741"
---
# <a name="nmisclassifications-function"></a>Функция Нмисклассификатионс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


При наличии набора выводимых меток и набора правильных меток возвращает количество индексов, в которых каждый набор меток различается.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="proposed--int"></a>предложено: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Количество индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .