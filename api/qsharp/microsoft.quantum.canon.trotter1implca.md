---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Операция Trotter1ImplCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 250b80729530a5d3054e037d9dd653904a57f6d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715300"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="79a42-102">Операция Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="79a42-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="79a42-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="79a42-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="79a42-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="79a42-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="79a42-105">Реализация первого порядка Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="79a42-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="79a42-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="79a42-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="79a42-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79a42-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79a42-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="79a42-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="79a42-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="79a42-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="79a42-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="79a42-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="79a42-111">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="79a42-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="79a42-112">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="79a42-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="79a42-113">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="79a42-113">target : 'T</span></span>

<span data-ttu-id="79a42-114">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="79a42-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79a42-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79a42-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="79a42-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="79a42-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="79a42-117">Е</span><span class="sxs-lookup"><span data-stu-id="79a42-117">'T</span></span>

<span data-ttu-id="79a42-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="79a42-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>