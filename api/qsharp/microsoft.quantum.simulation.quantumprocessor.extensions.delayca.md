---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.DelayCA
title: Операция Делайка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: DelayCA
qsharp.summary: ''
ms.openlocfilehash: 3b98cb25adc4e7b39a6139ce1631b1a4505a69bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857853"
---
# <a name="delayca-operation"></a><span data-ttu-id="2174c-102">Операция Делайка</span><span class="sxs-lookup"><span data-stu-id="2174c-102">DelayCA operation</span></span>

<span data-ttu-id="2174c-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="2174c-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="2174c-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2174c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2174c-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2174c-105">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="2174c-106">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="2174c-106">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="arg--t"></a><span data-ttu-id="2174c-107">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="2174c-107">arg : 'T</span></span>




### <a name="aux--unit"></a><span data-ttu-id="2174c-108">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2174c-108">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="2174c-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2174c-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2174c-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2174c-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2174c-111">Е</span><span class="sxs-lookup"><span data-stu-id="2174c-111">'T</span></span>

