---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Операция Апплисериесофопск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844648"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="96ed3-102">Операция Апплисериесофопск</span><span class="sxs-lookup"><span data-stu-id="96ed3-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="96ed3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="96ed3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="96ed3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="96ed3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="96ed3-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="96ed3-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="96ed3-106">Управляет</span><span class="sxs-lookup"><span data-stu-id="96ed3-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="96ed3-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="96ed3-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="96ed3-108">Листофопс: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL []</span><span class="sxs-lookup"><span data-stu-id="96ed3-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="96ed3-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="96ed3-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="96ed3-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="96ed3-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="96ed3-111">Каждый из них должен иметь управляемый функтор</span><span class="sxs-lookup"><span data-stu-id="96ed3-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="96ed3-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="96ed3-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="96ed3-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="96ed3-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="96ed3-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="96ed3-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="96ed3-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="96ed3-115">register : 'T[]</span></span>

<span data-ttu-id="96ed3-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="96ed3-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="96ed3-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="96ed3-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="96ed3-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="96ed3-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="96ed3-119">Е</span><span class="sxs-lookup"><span data-stu-id="96ed3-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="96ed3-120">Пример</span><span class="sxs-lookup"><span data-stu-id="96ed3-120">Example</span></span>

<span data-ttu-id="96ed3-121">Следующая команда применяет exp ([Пауликс, Паулий], 0,5) к Кубитс 0, 1//then X к кубит 2 Let Ops = [exp ([Пауликс, Паулий], 0,5, _), Апплитофирсткубитк (X, _)]; разрешить индексы = [[0, 1], [2]]; Апплисериесофопск (Ops, indices, Кубитаррай);</span><span class="sxs-lookup"><span data-stu-id="96ed3-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitC(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsC(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="96ed3-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="96ed3-122">See Also</span></span>

- [<span data-ttu-id="96ed3-123">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="96ed3-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)