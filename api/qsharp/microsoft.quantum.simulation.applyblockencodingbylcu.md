---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Операция Апплиблоккенкодингбилку
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: a9a9e3bbd598453719f49f78392f3a92c9401b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852829"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="69c6c-102">Операция Апплиблоккенкодингбилку</span><span class="sxs-lookup"><span data-stu-id="69c6c-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="69c6c-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="69c6c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="69c6c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="69c6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="69c6c-105">Реализация метода `BlockEncodingByLCU`.</span><span class="sxs-lookup"><span data-stu-id="69c6c-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="69c6c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="69c6c-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="69c6c-107">Статепрепаратион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="69c6c-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="69c6c-108">селектор: ('T) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="69c6c-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="69c6c-109">вспомогательная: 'T</span><span class="sxs-lookup"><span data-stu-id="69c6c-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="69c6c-110">система:</span><span class="sxs-lookup"><span data-stu-id="69c6c-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="69c6c-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="69c6c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="69c6c-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="69c6c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="69c6c-113">Е</span><span class="sxs-lookup"><span data-stu-id="69c6c-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="69c6c-114">Возникл</span><span class="sxs-lookup"><span data-stu-id="69c6c-114">'S</span></span>

