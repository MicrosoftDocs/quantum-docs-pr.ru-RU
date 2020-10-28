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
# <a name="featureregistersize-function"></a><span data-ttu-id="e18c1-102">Функция Феатуререгистерсизе</span><span class="sxs-lookup"><span data-stu-id="e18c1-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="e18c1-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e18c1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e18c1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e18c1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e18c1-105">Возвращает число Кубитс, необходимое для кодирования конкретного вектора компонентов.</span><span class="sxs-lookup"><span data-stu-id="e18c1-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="e18c1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e18c1-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="e18c1-107">Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e18c1-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e18c1-108">Пример вектора компонентов для кодирования в кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="e18c1-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="e18c1-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e18c1-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e18c1-110">Размер, необходимый для кодирования `sample` в кубит регистр, выраженный в виде числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e18c1-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>