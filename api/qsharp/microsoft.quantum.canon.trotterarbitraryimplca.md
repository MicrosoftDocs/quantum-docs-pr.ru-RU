---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Операция Троттерарбитраримплка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: bb93517a479ce344277bfe97d070e6630a8fccc0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840086"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="b598d-102">Операция Троттерарбитраримплка</span><span class="sxs-lookup"><span data-stu-id="b598d-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="b598d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b598d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b598d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b598d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b598d-105">Рекурсивная реализация Троттер-Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="b598d-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b598d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b598d-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="b598d-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b598d-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b598d-108">Порядок Trotter-Suzuki интегратора.</span><span class="sxs-lookup"><span data-stu-id="b598d-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="b598d-109">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b598d-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b598d-110">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="b598d-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="b598d-111">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="b598d-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b598d-112">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="b598d-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="b598d-113">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b598d-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b598d-114">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="b598d-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="b598d-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="b598d-115">target : 'T</span></span>

<span data-ttu-id="b598d-116">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="b598d-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b598d-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b598d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b598d-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b598d-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b598d-119">Е</span><span class="sxs-lookup"><span data-stu-id="b598d-119">'T</span></span>

<span data-ttu-id="b598d-120">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="b598d-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>