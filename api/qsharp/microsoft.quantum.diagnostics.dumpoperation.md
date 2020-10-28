---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Операция Думпоператион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712863"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="f87ed-102">Операция Думпоператион</span><span class="sxs-lookup"><span data-stu-id="f87ed-102">DumpOperation operation</span></span>

<span data-ttu-id="f87ed-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f87ed-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f87ed-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f87ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f87ed-105">При наличии операции отображает диагностику операции, которая стала доступной для текущего целевого объекта выполнения.</span><span class="sxs-lookup"><span data-stu-id="f87ed-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="f87ed-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f87ed-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f87ed-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f87ed-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f87ed-108">Число Кубитс, на которых действует данная операция.</span><span class="sxs-lookup"><span data-stu-id="f87ed-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit-adj"></a><span data-ttu-id="f87ed-109">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="f87ed-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f87ed-110">Операция, которую необходимо диагностировать.</span><span class="sxs-lookup"><span data-stu-id="f87ed-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f87ed-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f87ed-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f87ed-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="f87ed-112">Remarks</span></span>

<span data-ttu-id="f87ed-113">Вызов этой операции не имеет наблюдаемого воздействия в Q #.</span><span class="sxs-lookup"><span data-stu-id="f87ed-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="f87ed-114">Точная диагностика, отображаемая при их наличии, зависит от текущего целевого объекта выполнения и среды редактора.</span><span class="sxs-lookup"><span data-stu-id="f87ed-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="f87ed-115">Например, при использовании в симуляторе с полным состоянием отображается единая матрица, используемая для представления `op` .</span><span class="sxs-lookup"><span data-stu-id="f87ed-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="f87ed-116">Обратите внимание, что при запуске в симуляторах, которые приводят к неоднозначности глобального этапа (например, симулятор с полным состоянием), возвращаемые представления могут отличаться до глобального этапа.</span><span class="sxs-lookup"><span data-stu-id="f87ed-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="f87ed-117">Аналогичным образом, упорядочивание матричных представлений строк и столбцов может отличаться от соглашений, используемых каждым симулятором, поддерживающим эту операцию.</span><span class="sxs-lookup"><span data-stu-id="f87ed-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>