---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneC
title: Операция Апплифонек
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneC
qsharp.summary: ''
ms.openlocfilehash: d7c4e39ba26befeabad612e888da4abd00efaeb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230962"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="e0377-102">Операция Апплифонек</span><span class="sxs-lookup"><span data-stu-id="e0377-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="e0377-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="e0377-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="e0377-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e0377-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneC<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl), oneArg : 'T)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="e0377-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0377-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="e0377-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="e0377-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-ctl"></a><span data-ttu-id="e0377-107">Онресултонеоп: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="e0377-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="e0377-108">Онеарг: 'T</span><span class="sxs-lookup"><span data-stu-id="e0377-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="e0377-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0377-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e0377-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e0377-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e0377-111">Е</span><span class="sxs-lookup"><span data-stu-id="e0377-111">'T</span></span>

