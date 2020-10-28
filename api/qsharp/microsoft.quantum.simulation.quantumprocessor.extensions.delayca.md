---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.DelayCA
title: Операция Делайка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: DelayCA
qsharp.summary: ''
ms.openlocfilehash: 8bb33b9bfedcd324a2dea0ac9ab2a0ddadd6db20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734137"
---
# <a name="delayca-operation"></a><span data-ttu-id="ca783-102">Операция Делайка</span><span class="sxs-lookup"><span data-stu-id="ca783-102">DelayCA operation</span></span>

<span data-ttu-id="ca783-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="ca783-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="ca783-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca783-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="input"></a><span data-ttu-id="ca783-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ca783-105">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="ca783-106">Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="ca783-106">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="arg--t"></a><span data-ttu-id="ca783-107">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="ca783-107">arg : 'T</span></span>




### <a name="aux--unit"></a><span data-ttu-id="ca783-108">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca783-108">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="ca783-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca783-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ca783-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ca783-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ca783-111">Е</span><span class="sxs-lookup"><span data-stu-id="ca783-111">'T</span></span>

