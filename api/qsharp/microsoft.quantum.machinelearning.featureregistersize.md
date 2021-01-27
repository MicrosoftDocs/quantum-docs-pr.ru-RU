---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Функция Феатуререгистерсизе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 2754e901d74175c1841a38d795f5de02dabc9b8d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848439"
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