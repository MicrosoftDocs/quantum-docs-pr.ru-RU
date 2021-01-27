---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Операция Апплисериесофопса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: 052cb52d4ee6500e60043ab7f808497058924afe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844663"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="a67b2-102">Операция Апплисериесофопса</span><span class="sxs-lookup"><span data-stu-id="a67b2-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="a67b2-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a67b2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a67b2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a67b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a67b2-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="a67b2-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="a67b2-106">(Прилегающий)</span><span class="sxs-lookup"><span data-stu-id="a67b2-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a67b2-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a67b2-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="a67b2-108">Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []</span><span class="sxs-lookup"><span data-stu-id="a67b2-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="a67b2-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="a67b2-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="a67b2-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="a67b2-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="a67b2-111">Каждый должен иметь смежный функтор</span><span class="sxs-lookup"><span data-stu-id="a67b2-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="a67b2-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="a67b2-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="a67b2-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="a67b2-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="a67b2-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="a67b2-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="a67b2-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="a67b2-115">register : 'T[]</span></span>

<span data-ttu-id="a67b2-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="a67b2-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a67b2-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a67b2-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a67b2-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a67b2-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a67b2-119">Е</span><span class="sxs-lookup"><span data-stu-id="a67b2-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="a67b2-120">Пример</span><span class="sxs-lookup"><span data-stu-id="a67b2-120">Example</span></span>

<span data-ttu-id="a67b2-121">Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубита (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопса (Ops, indices, Кубитаррай);</span><span class="sxs-lookup"><span data-stu-id="a67b2-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="a67b2-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="a67b2-122">See Also</span></span>

- [<span data-ttu-id="a67b2-123">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="a67b2-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)