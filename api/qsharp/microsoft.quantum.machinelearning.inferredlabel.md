---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Функция Инферредлабел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848419"
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