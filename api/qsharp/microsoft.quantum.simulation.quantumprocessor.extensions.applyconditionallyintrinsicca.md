---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicCA
title: Операция Аппликондитионаллинтринсикка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 7cdddba45824d5e5037270d8578f2cb16c03be83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730857"
---
# <a name="applyconditionallyintrinsicca-operation"></a><span data-ttu-id="f83f1-102">Операция Аппликондитионаллинтринсикка</span><span class="sxs-lookup"><span data-stu-id="f83f1-102">ApplyConditionallyIntrinsicCA operation</span></span>

<span data-ttu-id="f83f1-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="f83f1-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="f83f1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f83f1-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicCA (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl + Adj), onNonEqualOp : (Unit => Unit is Ctl + Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="f83f1-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f83f1-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="f83f1-106">Меасурементресултс: __Недопустимый <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="f83f1-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="f83f1-107">Ресултсвалуес: __Недопустимый <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="f83f1-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--unit--unit-ctl--adj"></a><span data-ttu-id="f83f1-108">онекуалоп. единица [измерения](xref:microsoft.quantum.lang-ref.unit) : => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + года</span><span class="sxs-lookup"><span data-stu-id="f83f1-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="onnonequalop--unit--unit-ctl--adj"></a><span data-ttu-id="f83f1-109">оннонекуалоп. единица [измерения](xref:microsoft.quantum.lang-ref.unit) : => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + года</span><span class="sxs-lookup"><span data-stu-id="f83f1-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>





## <a name="output--unit"></a><span data-ttu-id="f83f1-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f83f1-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

