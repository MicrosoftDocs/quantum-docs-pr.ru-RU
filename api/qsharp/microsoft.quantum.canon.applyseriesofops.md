---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Операция Апплисериесофопс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841500"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="c2f3b-102">Операция Апплисериесофопс</span><span class="sxs-lookup"><span data-stu-id="c2f3b-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="c2f3b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c2f3b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c2f3b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2f3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2f3b-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c2f3b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2f3b-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="c2f3b-107">Листофопс: 'T [] = [модуль](xref:microsoft.quantum.lang-ref.unit)> []</span><span class="sxs-lookup"><span data-stu-id="c2f3b-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="c2f3b-108">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="c2f3b-109">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="c2f3b-110">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="c2f3b-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="c2f3b-111">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="c2f3b-112">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="c2f3b-113">Register: не []</span><span class="sxs-lookup"><span data-stu-id="c2f3b-113">register : 'T[]</span></span>

<span data-ttu-id="c2f3b-114">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="c2f3b-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2f3b-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2f3b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c2f3b-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c2f3b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c2f3b-117">Е</span><span class="sxs-lookup"><span data-stu-id="c2f3b-117">'T</span></span>



## <a name="example"></a><span data-ttu-id="c2f3b-118">Пример</span><span class="sxs-lookup"><span data-stu-id="c2f3b-118">Example</span></span>

<span data-ttu-id="c2f3b-119">Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубит (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопс (Ops, indices, Кубитаррай);</span><span class="sxs-lookup"><span data-stu-id="c2f3b-119">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubit(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOps(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="c2f3b-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="c2f3b-120">See Also</span></span>

- [<span data-ttu-id="c2f3b-121">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="c2f3b-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)