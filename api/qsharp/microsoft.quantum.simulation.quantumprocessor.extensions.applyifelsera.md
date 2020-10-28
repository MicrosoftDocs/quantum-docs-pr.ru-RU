---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRA
title: Операция Апплифелсера
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRA
qsharp.summary: ''
ms.openlocfilehash: bcc52c6e2b4dfc6354e12c57e19739ac021d2e8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734025"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="095b5-102">Операция Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="095b5-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="095b5-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="095b5-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="095b5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="095b5-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseRA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj), oneArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="095b5-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="095b5-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="095b5-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="095b5-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj"></a><span data-ttu-id="095b5-107">Онресултзеруп: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="095b5-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="095b5-108">Зероарг: 'T</span><span class="sxs-lookup"><span data-stu-id="095b5-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit-adj"></a><span data-ttu-id="095b5-109">Онресултонеоп: "U [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="095b5-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="onearg--u"></a><span data-ttu-id="095b5-110">Онеарг: ' U</span><span class="sxs-lookup"><span data-stu-id="095b5-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="095b5-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="095b5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="095b5-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="095b5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="095b5-113">Е</span><span class="sxs-lookup"><span data-stu-id="095b5-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="095b5-114">' U</span><span class="sxs-lookup"><span data-stu-id="095b5-114">'U</span></span>

