---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Функция Феатуререгистерсизе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732809"
---
# <a name="featureregistersize-function"></a>Функция Феатуререгистерсизе

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


Возвращает число Кубитс, необходимое для кодирования конкретного вектора компонентов.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="sample--double"></a>Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]

Пример вектора компонентов для кодирования в кубит регистр.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Размер, необходимый для кодирования `sample` в кубит регистр, выраженный в виде числа Кубитс.