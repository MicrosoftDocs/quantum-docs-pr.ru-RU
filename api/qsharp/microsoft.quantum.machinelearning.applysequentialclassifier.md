---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Операция Апплисекуентиалклассифиер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: fe1ca5717f18cc0816b96ddd29ce89c568571791
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212024"
---
# <a name="applysequentialclassifier-operation"></a>Операция Апплисекуентиалклассифиер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Учитывая структуру и параметризацию последовательного классификатора, применяет классификатор к регистру Кубитс.

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)




### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Целевой регистр, к которому должен применяться классификатор.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

