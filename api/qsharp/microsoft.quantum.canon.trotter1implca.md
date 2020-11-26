---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Операция Trotter1ImplCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1b4e0a9597f4f30b8e92ef91ff0780e7c7ecdc9b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204799"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="af297-102">Операция Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="af297-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="af297-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="af297-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="af297-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af297-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af297-105">Реализация первого порядка Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="af297-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="af297-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="af297-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="af297-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="af297-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="af297-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="af297-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="af297-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="af297-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="af297-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="af297-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="af297-111">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af297-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af297-112">Множитель по размеру каждого этапа моделирования.</span><span class="sxs-lookup"><span data-stu-id="af297-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="af297-113">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="af297-113">target : 'T</span></span>

<span data-ttu-id="af297-114">Регистр такта, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="af297-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af297-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af297-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="af297-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="af297-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="af297-117">Е</span><span class="sxs-lookup"><span data-stu-id="af297-117">'T</span></span>

<span data-ttu-id="af297-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="af297-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>