---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Операция Апплифелсерк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 21069c43c16bc9712973ac4e0afea8320c0d83a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709462"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="24f07-102">Операция Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="24f07-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="24f07-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="24f07-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="24f07-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24f07-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="24f07-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="24f07-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="24f07-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="24f07-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-ctl"></a><span data-ttu-id="24f07-107">Онресултзеруп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="24f07-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="24f07-108">Зероарг: 'T</span><span class="sxs-lookup"><span data-stu-id="24f07-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit-ctl"></a><span data-ttu-id="24f07-109">Онресултонеоп: "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="24f07-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="24f07-110">Онеарг: ' U</span><span class="sxs-lookup"><span data-stu-id="24f07-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="24f07-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="24f07-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="24f07-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="24f07-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="24f07-113">Е</span><span class="sxs-lookup"><span data-stu-id="24f07-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="24f07-114">' U</span><span class="sxs-lookup"><span data-stu-id="24f07-114">'U</span></span>

