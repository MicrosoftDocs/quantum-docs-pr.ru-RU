---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Операция Апплиблоккенкодингбилку
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732145"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="65c59-102">Операция Апплиблоккенкодингбилку</span><span class="sxs-lookup"><span data-stu-id="65c59-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="65c59-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="65c59-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="65c59-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="65c59-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="65c59-105">Реализация метода `BlockEncodingByLCU`.</span><span class="sxs-lookup"><span data-stu-id="65c59-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a><span data-ttu-id="65c59-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65c59-106">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="65c59-107">Статепрепаратион: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="65c59-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="65c59-108">селектор: ('T) [=>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия</span><span class="sxs-lookup"><span data-stu-id="65c59-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="65c59-109">вспомогательная: 'T</span><span class="sxs-lookup"><span data-stu-id="65c59-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="65c59-110">система:</span><span class="sxs-lookup"><span data-stu-id="65c59-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="65c59-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="65c59-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="65c59-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="65c59-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="65c59-113">Е</span><span class="sxs-lookup"><span data-stu-id="65c59-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="65c59-114">Возникл</span><span class="sxs-lookup"><span data-stu-id="65c59-114">'S</span></span>

