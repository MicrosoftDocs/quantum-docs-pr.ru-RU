---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Функция Жетженераторсистемфунктион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 7b6eabd203cecf8c64f0bff3e06f08a0bec31bf2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852770"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="4140f-102">Функция Жетженераторсистемфунктион</span><span class="sxs-lookup"><span data-stu-id="4140f-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="4140f-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4140f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4140f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4140f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4140f-105">Извлекает `GeneratorIndex` функцию в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="4140f-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="4140f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4140f-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="4140f-107">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="4140f-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="4140f-108">Необходимый объект `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="4140f-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="4140f-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="4140f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="4140f-110">Функция, которая индексирует каждый `GeneratorIndex` термин в хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="4140f-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="4140f-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="4140f-111">See Also</span></span>

- [<span data-ttu-id="4140f-112">Microsoft. тактов. моделирование. Женераториндекс</span><span class="sxs-lookup"><span data-stu-id="4140f-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="4140f-113">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="4140f-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)