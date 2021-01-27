---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Операция Trotter2ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852017"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="abc79-102">Операция Trotter2ImplCA</span><span class="sxs-lookup"><span data-stu-id="abc79-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="abc79-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="abc79-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="abc79-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="abc79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="abc79-105">Реализация второго порядка Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="abc79-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="abc79-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="abc79-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="abc79-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="abc79-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="abc79-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="abc79-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="abc79-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="abc79-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="abc79-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="abc79-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="abc79-111">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="abc79-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="abc79-112">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="abc79-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="abc79-113">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="abc79-113">target : 'T</span></span>

<span data-ttu-id="abc79-114">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="abc79-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="abc79-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="abc79-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="abc79-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="abc79-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="abc79-117">Е</span><span class="sxs-lookup"><span data-stu-id="abc79-117">'T</span></span>

<span data-ttu-id="abc79-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="abc79-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="abc79-119">Пример</span><span class="sxs-lookup"><span data-stu-id="abc79-119">Example</span></span>

<span data-ttu-id="abc79-120">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="abc79-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

<span data-ttu-id="abc79-121">и</span><span class="sxs-lookup"><span data-stu-id="abc79-121">and</span></span>

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```