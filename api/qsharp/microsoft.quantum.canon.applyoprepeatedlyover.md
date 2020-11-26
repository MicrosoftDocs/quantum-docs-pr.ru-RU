---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Операция Апплйопрепеатедлйовер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 343392d5a6af07cdc45fd8bab6656d59a6f2b350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218314"
---
# <a name="applyoprepeatedlyover-operation"></a><span data-ttu-id="ae4ef-102">Операция Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="ae4ef-102">ApplyOpRepeatedlyOver operation</span></span>

<span data-ttu-id="ae4ef-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae4ef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae4ef-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae4ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae4ef-105">Применяет одну и ту же Op к кубит регистру несколько раз.</span><span class="sxs-lookup"><span data-stu-id="ae4ef-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ae4ef-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ae4ef-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="ae4ef-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="ae4ef-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ae4ef-108">Операция, которая должна быть применена несколько раз к регистру кубит</span><span class="sxs-lookup"><span data-stu-id="ae4ef-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="ae4ef-109">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="ae4ef-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="ae4ef-110">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="ae4ef-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="ae4ef-111">Каждый массив должен содержать список ints, описывающих используемый Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ae4ef-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ae4ef-112">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ae4ef-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ae4ef-113">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="ae4ef-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae4ef-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae4ef-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ae4ef-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="ae4ef-115">See Also</span></span>

- [<span data-ttu-id="ae4ef-116">Microsoft. тактов. Canon. Апплисериесофопс</span><span class="sxs-lookup"><span data-stu-id="ae4ef-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)