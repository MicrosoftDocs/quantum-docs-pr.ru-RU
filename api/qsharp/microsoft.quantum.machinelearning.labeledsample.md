---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846980"
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