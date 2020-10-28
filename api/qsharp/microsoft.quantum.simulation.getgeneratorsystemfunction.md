---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Функция Жетженераторсистемфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733536"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="3d63c-102">Функция Жетженераторсистемфунктион</span><span class="sxs-lookup"><span data-stu-id="3d63c-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="3d63c-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="3d63c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="3d63c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3d63c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3d63c-105">Извлекает `GeneratorIndex` функцию в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="3d63c-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="3d63c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d63c-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="3d63c-107">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="3d63c-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="3d63c-108">Необходимый объект `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="3d63c-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="3d63c-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3d63c-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3d63c-110">Функция, которая индексирует каждый `GeneratorIndex` термин в хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="3d63c-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d63c-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="3d63c-111">See Also</span></span>

- [<span data-ttu-id="3d63c-112">Microsoft. тактов. моделирование. Женераториндекс</span><span class="sxs-lookup"><span data-stu-id="3d63c-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="3d63c-113">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="3d63c-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)