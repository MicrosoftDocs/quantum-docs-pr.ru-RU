---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverCA
title: Операция Апплйопрепеатедлйоверка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverCA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: b7d401f323d7affc27697744bb659c687e252682
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209116"
---
# <a name="applyoprepeatedlyoverca-operation"></a><span data-ttu-id="c9963-102">Операция Апплйопрепеатедлйоверка</span><span class="sxs-lookup"><span data-stu-id="c9963-102">ApplyOpRepeatedlyOverCA operation</span></span>

<span data-ttu-id="c9963-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c9963-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c9963-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c9963-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c9963-105">Применяет одну и ту же Op к кубит регистру несколько раз.</span><span class="sxs-lookup"><span data-stu-id="c9963-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverCA (op : (Qubit[] => Unit is Adj + Ctl), targets : Int[][], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c9963-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c9963-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="c9963-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="c9963-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="c9963-108">Операция, которая должна быть применена несколько раз к регистру кубит</span><span class="sxs-lookup"><span data-stu-id="c9963-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="c9963-109">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="c9963-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="c9963-110">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="c9963-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="c9963-111">Каждый массив должен содержать список ints, описывающих используемый Кубитс.</span><span class="sxs-lookup"><span data-stu-id="c9963-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c9963-112">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c9963-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c9963-113">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="c9963-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c9963-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c9963-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c9963-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="c9963-115">See Also</span></span>

- [<span data-ttu-id="c9963-116">Microsoft. тактов. Canon. Апплисериесофопс</span><span class="sxs-lookup"><span data-stu-id="c9963-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)