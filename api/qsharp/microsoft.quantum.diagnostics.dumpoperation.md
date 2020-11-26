---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Операция Думпоператион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: b0e07173ddbeb8a96d4a85928258b6e30deb394d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202062"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="e3b42-102">Операция Думпоператион</span><span class="sxs-lookup"><span data-stu-id="e3b42-102">DumpOperation operation</span></span>

<span data-ttu-id="e3b42-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e3b42-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e3b42-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3b42-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3b42-105">При наличии операции отображает диагностику операции, которая стала доступной для текущего целевого объекта выполнения.</span><span class="sxs-lookup"><span data-stu-id="e3b42-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="e3b42-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e3b42-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="e3b42-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3b42-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3b42-108">Число Кубитс, на которых действует данная операция.</span><span class="sxs-lookup"><span data-stu-id="e3b42-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="e3b42-109">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="e3b42-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e3b42-110">Операция, которую необходимо диагностировать.</span><span class="sxs-lookup"><span data-stu-id="e3b42-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3b42-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3b42-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e3b42-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3b42-112">Remarks</span></span>

<span data-ttu-id="e3b42-113">Вызов этой операции не имеет наблюдаемого воздействия в Q #.</span><span class="sxs-lookup"><span data-stu-id="e3b42-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="e3b42-114">Точная диагностика, отображаемая при их наличии, зависит от текущего целевого объекта выполнения и среды редактора.</span><span class="sxs-lookup"><span data-stu-id="e3b42-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="e3b42-115">Например, при использовании в симуляторе с полным состоянием отображается единая матрица, используемая для представления `op` .</span><span class="sxs-lookup"><span data-stu-id="e3b42-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="e3b42-116">Обратите внимание, что при запуске в симуляторах, которые приводят к неоднозначности глобального этапа (например, симулятор с полным состоянием), возвращаемые представления могут отличаться до глобального этапа.</span><span class="sxs-lookup"><span data-stu-id="e3b42-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="e3b42-117">Аналогичным образом, упорядочивание матричных представлений строк и столбцов может отличаться от соглашений, используемых каждым симулятором, поддерживающим эту операцию.</span><span class="sxs-lookup"><span data-stu-id="e3b42-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>