---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Функция Инферредлабелс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848397"
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