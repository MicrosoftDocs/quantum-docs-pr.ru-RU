---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Операция Троттерарбитраримплка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1c094d09ac8bdd71a59ef57d8715a6f90f18efc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715286"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="74140-102">Операция Троттерарбитраримплка</span><span class="sxs-lookup"><span data-stu-id="74140-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="74140-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="74140-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="74140-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74140-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74140-105">Рекурсивная реализация Троттер-Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="74140-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="74140-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="74140-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="74140-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74140-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74140-108">Порядок Trotter-Suzuki интегратора.</span><span class="sxs-lookup"><span data-stu-id="74140-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="74140-109">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74140-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74140-110">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="74140-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="74140-111">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="74140-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="74140-112">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="74140-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="74140-113">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="74140-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="74140-114">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="74140-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="74140-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="74140-115">target : 'T</span></span>

<span data-ttu-id="74140-116">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="74140-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74140-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74140-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="74140-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="74140-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="74140-119">Е</span><span class="sxs-lookup"><span data-stu-id="74140-119">'T</span></span>

<span data-ttu-id="74140-120">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="74140-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>