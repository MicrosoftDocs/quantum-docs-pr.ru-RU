---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Функция ошибок классификации
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853931"
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

## <a name="example"></a>Пример

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```