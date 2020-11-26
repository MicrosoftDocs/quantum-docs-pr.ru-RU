---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196333"
---
# <a name="labeledsample-user-defined-type"></a>Определяемый пользователем тип Лабеледсампле

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Пример с именем класса, к которому принадлежит образец.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="features--double"></a>Функции: [Double](xref:microsoft.quantum.lang-ref.double)[]

Вектор функций для данного примера.
### <a name="label--int"></a>Метка: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленная метка для класса, к которому принадлежит этот образец.