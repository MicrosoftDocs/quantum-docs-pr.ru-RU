---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Операция Апплиблоккенкодингбилку
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 8ce6eb16b1dc5a83dd3a9559592c20d6b7b999b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225489"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="c1d4b-102">Операция Апплиблоккенкодингбилку</span><span class="sxs-lookup"><span data-stu-id="c1d4b-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="c1d4b-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c1d4b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c1d4b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c1d4b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c1d4b-105">Реализация метода `BlockEncodingByLCU`.</span><span class="sxs-lookup"><span data-stu-id="c1d4b-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c1d4b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c1d4b-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="c1d4b-107">Статепрепаратион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="c1d4b-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="c1d4b-108">селектор: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="c1d4b-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="c1d4b-109">вспомогательная: 'T</span><span class="sxs-lookup"><span data-stu-id="c1d4b-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="c1d4b-110">система:</span><span class="sxs-lookup"><span data-stu-id="c1d4b-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="c1d4b-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1d4b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c1d4b-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c1d4b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c1d4b-113">Е</span><span class="sxs-lookup"><span data-stu-id="c1d4b-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="c1d4b-114">Возникл</span><span class="sxs-lookup"><span data-stu-id="c1d4b-114">'S</span></span>

