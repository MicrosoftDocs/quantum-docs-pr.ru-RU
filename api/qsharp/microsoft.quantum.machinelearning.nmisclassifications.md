---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Функция Нмисклассификатионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: adc7042d6108c7ec72d13340633824d3eaf5e18e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853902"
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

## <a name="example"></a>Пример

```qsharp
let nMisclassifications = NMisclassifications([1, 1, 0, 0], [0, 1, 1, 0]);
Message($"{nMisclassifications}"); // Will print 2.
```