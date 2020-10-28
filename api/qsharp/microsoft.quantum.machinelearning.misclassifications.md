---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Функция ошибок классификации
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732977"
---
# <a name="misclassifications-function"></a>Функция ошибок классификации

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


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