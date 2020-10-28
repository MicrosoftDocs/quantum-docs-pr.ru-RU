---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Операция Апплифзероа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 124c5bbabc9e22804734ddbde955312db9655187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734192"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="5a0de-102">Операция Апплифзероа</span><span class="sxs-lookup"><span data-stu-id="5a0de-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="5a0de-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="5a0de-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="5a0de-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a0de-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="5a0de-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a0de-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="5a0de-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="5a0de-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj"></a><span data-ttu-id="5a0de-107">Онресултзеруп: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="5a0de-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="5a0de-108">Зероарг: 'T</span><span class="sxs-lookup"><span data-stu-id="5a0de-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="5a0de-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a0de-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5a0de-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5a0de-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a0de-111">Е</span><span class="sxs-lookup"><span data-stu-id="5a0de-111">'T</span></span>

