---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Операция Думпоператион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829273"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="846a8-102">Операция Думпоператион</span><span class="sxs-lookup"><span data-stu-id="846a8-102">DumpOperation operation</span></span>

<span data-ttu-id="846a8-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="846a8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="846a8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="846a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="846a8-105">При наличии операции отображает диагностику операции, которая стала доступной для текущего целевого объекта выполнения.</span><span class="sxs-lookup"><span data-stu-id="846a8-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="846a8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="846a8-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="846a8-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="846a8-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="846a8-108">Число Кубитс, на которых действует данная операция.</span><span class="sxs-lookup"><span data-stu-id="846a8-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="846a8-109">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="846a8-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="846a8-110">Операция, которую необходимо диагностировать.</span><span class="sxs-lookup"><span data-stu-id="846a8-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="846a8-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="846a8-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="846a8-112">Пример</span><span class="sxs-lookup"><span data-stu-id="846a8-112">Example</span></span>

<span data-ttu-id="846a8-113">При запуске на целевом объекте такта имитатора следующий фрагмент выводит матрицу $ $ \бегин{алигнед} \лефт (\бегин{Матрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \енд{Матрикс}\ригхт) \енд{алигнед}.</span><span class="sxs-lookup"><span data-stu-id="846a8-113">When run on the quantum simulator target, the following snippet will output the matrix $$ \begin{aligned} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \end{matrix}\right) \end{aligned}.</span></span>
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a><span data-ttu-id="846a8-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="846a8-114">Remarks</span></span>

<span data-ttu-id="846a8-115">Вызов этой операции не имеет наблюдаемого воздействия в Q #.</span><span class="sxs-lookup"><span data-stu-id="846a8-115">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="846a8-116">Точная диагностика, отображаемая при их наличии, зависит от текущего целевого объекта выполнения и среды редактора.</span><span class="sxs-lookup"><span data-stu-id="846a8-116">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="846a8-117">Например, при использовании в симуляторе с полным состоянием отображается единая матрица, используемая для представления `op` .</span><span class="sxs-lookup"><span data-stu-id="846a8-117">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="846a8-118">Обратите внимание, что при запуске в симуляторах, которые приводят к неоднозначности глобального этапа (например, симулятор с полным состоянием), возвращаемые представления могут отличаться до глобального этапа.</span><span class="sxs-lookup"><span data-stu-id="846a8-118">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="846a8-119">Аналогичным образом, упорядочивание матричных представлений строк и столбцов может отличаться от соглашений, используемых каждым симулятором, поддерживающим эту операцию.</span><span class="sxs-lookup"><span data-stu-id="846a8-119">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>