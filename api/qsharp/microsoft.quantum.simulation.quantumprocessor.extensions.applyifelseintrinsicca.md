---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicCA
title: Операция Апплифелсеинтринсикка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: f8989a74b5719a41ab3688712f4bf5f61c85de8b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733664"
---
# <a name="applyifelseintrinsicca-operation"></a><span data-ttu-id="02d8d-102">Операция Апплифелсеинтринсикка</span><span class="sxs-lookup"><span data-stu-id="02d8d-102">ApplyIfElseIntrinsicCA operation</span></span>

<span data-ttu-id="02d8d-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="02d8d-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="02d8d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="02d8d-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseIntrinsicCA (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl + Adj), onResultOneOp : (Unit => Unit is Ctl + Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="02d8d-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="02d8d-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="02d8d-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="02d8d-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--unit--unit-ctl--adj"></a><span data-ttu-id="02d8d-107">онресултзеруп. единица [измерения](xref:microsoft.quantum.lang-ref.unit) : => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + года</span><span class="sxs-lookup"><span data-stu-id="02d8d-107">onResultZeroOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="onresultoneop--unit--unit-ctl--adj"></a><span data-ttu-id="02d8d-108">онресултонеоп. единица [измерения](xref:microsoft.quantum.lang-ref.unit) : => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + года</span><span class="sxs-lookup"><span data-stu-id="02d8d-108">onResultOneOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>





## <a name="output--unit"></a><span data-ttu-id="02d8d-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02d8d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

