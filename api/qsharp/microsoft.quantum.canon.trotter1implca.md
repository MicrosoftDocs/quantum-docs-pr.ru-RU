---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Операция Trotter1ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 6de4b6e7a34d66037d83a6e2bd5821402207c743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840101"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="5a1d7-102">Операция Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="5a1d7-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="5a1d7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5a1d7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5a1d7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1d7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a1d7-105">Реализация первого порядка Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="5a1d7-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5a1d7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a1d7-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="5a1d7-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a1d7-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a1d7-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="5a1d7-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="5a1d7-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="5a1d7-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5a1d7-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="5a1d7-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="5a1d7-111">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a1d7-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a1d7-112">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="5a1d7-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="5a1d7-113">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="5a1d7-113">target : 'T</span></span>

<span data-ttu-id="5a1d7-114">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="5a1d7-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a1d7-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a1d7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5a1d7-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5a1d7-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a1d7-117">Е</span><span class="sxs-lookup"><span data-stu-id="5a1d7-117">'T</span></span>

<span data-ttu-id="5a1d7-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="5a1d7-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="5a1d7-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5a1d7-119">Example</span></span>

<span data-ttu-id="5a1d7-120">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5a1d7-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT, target);
op(1, deltaT, target);
```

<span data-ttu-id="5a1d7-121">и</span><span class="sxs-lookup"><span data-stu-id="5a1d7-121">and</span></span>

```qsharp
Trotter1ImplCA((2, op), deltaT, target);
```