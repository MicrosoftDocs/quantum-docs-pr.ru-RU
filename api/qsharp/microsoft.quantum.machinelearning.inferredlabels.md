---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Функция Инферредлабелс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 668ab89ed45c49d33ce50ff5d892f4d57246c12a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196367"
---
# <a name="inferredlabels-function"></a>Функция Инферредлабелс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии массива вероятностей классификации и смещения возвращает метку, выведенную из каждой вероятности.

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="bias--double"></a>уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)

Сдвиг между двумя классами, как правило, результатом обучения классификатора.


### <a name="probabilities--double"></a>вероятности: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив вероятностей классификации для набора выборок, обычно в результате оценки частоты классификации.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Метка выводится из каждой вероятности классификации.