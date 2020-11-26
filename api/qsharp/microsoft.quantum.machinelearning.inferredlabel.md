---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Функция Инферредлабел
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: b64bb1ec52d2456ee1b627b920890223d173533b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211786"
---
# <a name="inferredlabel-function"></a>Функция Инферредлабел

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии вероятности классификации и смещения возвращает метку, выведенную из этой вероятности.

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a>Входные данные

### <a name="bias--double"></a>уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)

Сдвиг между двумя классами, как правило, результатом обучения классификатора.


### <a name="probability--double"></a>вероятность: [Double](xref:microsoft.quantum.lang-ref.double)

Вероятности классификации для конкретного примера, которые обычно являются результатом оценки частоты классификации.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Метка, выводимая из данной вероятности классификации.