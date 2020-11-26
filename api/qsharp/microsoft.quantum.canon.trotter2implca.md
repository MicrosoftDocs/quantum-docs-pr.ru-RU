---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Операция Trotter2ImplCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 0e3a7e53a4d415e6b5af81d9bb3f52cddf36c4b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204748"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="678a9-102">Операция Trotter2ImplCA</span><span class="sxs-lookup"><span data-stu-id="678a9-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="678a9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="678a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="678a9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="678a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="678a9-105">Реализация второго порядка Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="678a9-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="678a9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="678a9-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="678a9-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="678a9-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="678a9-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="678a9-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="678a9-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="678a9-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="678a9-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="678a9-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="678a9-111">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="678a9-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="678a9-112">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="678a9-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="678a9-113">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="678a9-113">target : 'T</span></span>

<span data-ttu-id="678a9-114">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="678a9-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="678a9-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="678a9-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="678a9-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="678a9-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="678a9-117">Е</span><span class="sxs-lookup"><span data-stu-id="678a9-117">'T</span></span>

<span data-ttu-id="678a9-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="678a9-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>