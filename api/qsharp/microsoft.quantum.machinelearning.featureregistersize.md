---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Функция Феатуререгистерсизе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: bc5d5a23cfb431f9506b15bc404ab6955d1c2a35
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196418"
---
# <a name="featureregistersize-function"></a>Функция Феатуререгистерсизе

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Возвращает число Кубитс, необходимое для кодирования конкретного вектора компонентов.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="sample--double"></a>Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]

Пример вектора компонентов для кодирования в кубит регистр.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Размер, необходимый для кодирования `sample` в кубит регистр, выраженный в виде числа Кубитс.