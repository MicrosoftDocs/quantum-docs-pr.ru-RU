---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Операция Аппликондитионалли
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: 24d52576d2fb3e83f294874be4b0d1cd6a80f188
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229075"
---
# <a name="applyconditionally-operation"></a><span data-ttu-id="0686c-102">Операция Аппликондитионалли</span><span class="sxs-lookup"><span data-stu-id="0686c-102">ApplyConditionally operation</span></span>

<span data-ttu-id="0686c-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="0686c-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="0686c-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0686c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="0686c-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0686c-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="0686c-106">Меасурементресултс: __Недопустимый <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="0686c-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="0686c-107">Ресултсвалуес: __Недопустимый <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="0686c-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--t--unit"></a><span data-ttu-id="0686c-108">Онекуалоп: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="0686c-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="equalarg--t"></a><span data-ttu-id="0686c-109">Екуаларг: 'T</span><span class="sxs-lookup"><span data-stu-id="0686c-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit"></a><span data-ttu-id="0686c-110">Оннонекуалоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="0686c-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="nonequalarg--u"></a><span data-ttu-id="0686c-111">Нонекуаларг: ' U</span><span class="sxs-lookup"><span data-stu-id="0686c-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="0686c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0686c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0686c-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0686c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0686c-114">Е</span><span class="sxs-lookup"><span data-stu-id="0686c-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="0686c-115">' U</span><span class="sxs-lookup"><span data-stu-id="0686c-115">'U</span></span>

