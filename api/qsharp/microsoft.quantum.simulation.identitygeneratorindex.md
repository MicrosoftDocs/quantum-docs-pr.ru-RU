---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Функция Идентитиженераториндекс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733528"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="e0825-102">Функция Идентитиженераториндекс</span><span class="sxs-lookup"><span data-stu-id="e0825-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="e0825-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e0825-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e0825-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e0825-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e0825-105">Возвращает индекс генератора, совместимый с нулевым Хамилтониан, `H = 0` который соответствует операции эволюции идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="e0825-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="e0825-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0825-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="e0825-107">Идкстерм: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e0825-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e0825-108">Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.simulation.generatorsystem> определяемым пользователем типом.</span><span class="sxs-lookup"><span data-stu-id="e0825-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="e0825-109">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e0825-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e0825-110">Индекс генератора, представляющий развитие в Хамилтониан $H = $0.</span><span class="sxs-lookup"><span data-stu-id="e0825-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>