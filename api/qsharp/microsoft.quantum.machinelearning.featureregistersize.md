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
# <a name="featureregistersize-function"></a><span data-ttu-id="28948-102">Функция Феатуререгистерсизе</span><span class="sxs-lookup"><span data-stu-id="28948-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="28948-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="28948-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="28948-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="28948-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="28948-105">Возвращает число Кубитс, необходимое для кодирования конкретного вектора компонентов.</span><span class="sxs-lookup"><span data-stu-id="28948-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="28948-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28948-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="28948-107">Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="28948-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="28948-108">Пример вектора компонентов для кодирования в кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="28948-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="28948-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28948-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28948-110">Размер, необходимый для кодирования `sample` в кубит регистр, выраженный в виде числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="28948-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>