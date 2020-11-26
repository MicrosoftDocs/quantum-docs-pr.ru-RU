---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Функция Сумженераторсистемс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 7cb18e161dce3a52d7c9a0bf6a45d4818db2b849
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192474"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="34ced-102">Функция Сумженераторсистемс</span><span class="sxs-lookup"><span data-stu-id="34ced-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="34ced-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="34ced-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="34ced-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34ced-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34ced-105">Добавляет несколько объектов `GeneratorSystem` для создания нового женераторсистем.</span><span class="sxs-lookup"><span data-stu-id="34ced-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="34ced-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34ced-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="34ced-107">Женераторсистемс: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="34ced-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="34ced-108">Массив типа `GeneratorSystem[]`.</span><span class="sxs-lookup"><span data-stu-id="34ced-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="34ced-109">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="34ced-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="34ced-110">Объект `GeneratorSystem` , представляющий систему, которая является суммой систем генератора входных данных.</span><span class="sxs-lookup"><span data-stu-id="34ced-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="34ced-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="34ced-111">See Also</span></span>

- [<span data-ttu-id="34ced-112">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="34ced-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)