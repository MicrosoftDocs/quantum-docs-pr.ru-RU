---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Функция Нмисклассификатионс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 30d049ba54630cd2f5f350280bad7f587599f459
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196316"
---
# <a name="nmisclassifications-function"></a>Функция Нмисклассификатионс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии набора выводимых меток и набора правильных меток возвращает количество индексов, в которых каждый набор меток различается.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="proposed--int"></a>предложено: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Количество индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .