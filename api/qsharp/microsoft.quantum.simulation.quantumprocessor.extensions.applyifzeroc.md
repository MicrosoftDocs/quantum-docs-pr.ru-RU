---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: Операция Апплифзерок
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: 6de4fcf86495136f2caec6fb6f873a18d751c977
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734184"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="7aa04-102">Операция Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="7aa04-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="7aa04-103">Пространство имен: [Microsoft. тактов. симулятор. куантумпроцессор. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="7aa04-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="7aa04-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7aa04-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="7aa04-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7aa04-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="7aa04-106">Меасурементресулт: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="7aa04-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-ctl"></a><span data-ttu-id="7aa04-107">Онресултзеруп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="7aa04-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="7aa04-108">Зероарг: 'T</span><span class="sxs-lookup"><span data-stu-id="7aa04-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="7aa04-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7aa04-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7aa04-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7aa04-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7aa04-111">Е</span><span class="sxs-lookup"><span data-stu-id="7aa04-111">'T</span></span>

