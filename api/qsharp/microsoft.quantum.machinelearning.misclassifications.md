---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Функция ошибок классификации
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211684"
---
# <a name="misclassifications-function"></a>Функция ошибок классификации

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии набора выводимых меток и набора правильных меток возвращает индексы, где каждый набор меток отличается.

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="inferredlabels--int"></a>Инферредлабелс: [int](xref:microsoft.quantum.lang-ref.int)[]

Метки, выводимые для заданного обучения или набора проверки.


### <a name="actuallabels--int"></a>Актуаллабелс: [int](xref:microsoft.quantum.lang-ref.int)[]

Истинные метки для заданного обучения или набора проверки.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .