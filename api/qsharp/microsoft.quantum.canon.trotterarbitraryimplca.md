---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Операция Троттерарбитраримплка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 2abfbb9d51a98d8ede1b0835875a3771ffda0691
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204731"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="9e524-102">Операция Троттерарбитраримплка</span><span class="sxs-lookup"><span data-stu-id="9e524-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="9e524-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e524-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e524-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e524-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e524-105">Рекурсивная реализация Троттер-Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="9e524-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9e524-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9e524-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="9e524-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e524-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e524-108">Порядок Trotter-Suzuki интегратора.</span><span class="sxs-lookup"><span data-stu-id="9e524-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="9e524-109">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e524-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e524-110">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="9e524-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="9e524-111">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="9e524-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9e524-112">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="9e524-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="9e524-113">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9e524-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9e524-114">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="9e524-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="9e524-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="9e524-115">target : 'T</span></span>

<span data-ttu-id="9e524-116">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="9e524-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9e524-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9e524-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9e524-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9e524-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e524-119">Е</span><span class="sxs-lookup"><span data-stu-id="9e524-119">'T</span></span>

<span data-ttu-id="9e524-120">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="9e524-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>