---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: Функция Дефаулттраинингоптионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855993"
---
# <a name="defaulttrainingoptions-function"></a>Функция Дефаулттраинингоптионс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Возвращает набор параметров по умолчанию для учебных классификаторов.

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a>Выходные данные: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Разумный набор параметров обучения по умолчанию для использования при обучении классификаторов.

## <a name="example"></a>Пример

Чтобы использовать параметры по умолчанию, но с дополнительными измерениями, используйте `w/` оператор:

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```