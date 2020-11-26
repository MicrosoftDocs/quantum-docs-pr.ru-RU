---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: Функция Нкубитсрекуиред
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: e910edb9bf432e6acb5c349ee6b9d65797aaaba7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211667"
---
# <a name="nqubitsrequired-function"></a>Функция Нкубитсрекуиред

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Возвращает число Кубитс, необходимое для применения заданного последовательного классификатора.

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a>Входные данные

### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Минимальный размер регистра, на который может быть применен последовательный классификатор.