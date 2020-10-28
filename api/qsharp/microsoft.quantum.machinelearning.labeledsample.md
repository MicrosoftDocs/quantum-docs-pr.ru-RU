---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711337"
---
# <a name="labeledsample-user-defined-type"></a>Определяемый пользователем тип Лабеледсампле

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


Пример с именем класса, к которому принадлежит образец.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="features--double"></a>Функции: [Double](xref:microsoft.quantum.lang-ref.double)[]

Вектор функций для данного примера.
### <a name="label--int"></a>Метка: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленная метка для класса, к которому принадлежит этот образец.