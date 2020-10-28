---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Операция Апплйопрепеатедлйоверк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: effd61e6c012dcf81a83383c3fd43cf745d18117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717833"
---
# <a name="applyoprepeatedlyoverc-operation"></a><span data-ttu-id="db09f-102">Операция Апплйопрепеатедлйоверк</span><span class="sxs-lookup"><span data-stu-id="db09f-102">ApplyOpRepeatedlyOverC operation</span></span>

<span data-ttu-id="db09f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="db09f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="db09f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="db09f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="db09f-105">Применяет одну и ту же Op к кубит регистру несколько раз.</span><span class="sxs-lookup"><span data-stu-id="db09f-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="db09f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="db09f-106">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="db09f-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = Ctl [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="db09f-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="db09f-108">Операция, которая должна быть применена несколько раз к регистру кубит</span><span class="sxs-lookup"><span data-stu-id="db09f-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="db09f-109">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="db09f-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="db09f-110">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="db09f-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="db09f-111">Каждый массив должен содержать список ints, описывающих используемый Кубитс.</span><span class="sxs-lookup"><span data-stu-id="db09f-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="db09f-112">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="db09f-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="db09f-113">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="db09f-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="db09f-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="db09f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="db09f-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="db09f-115">See Also</span></span>

- [<span data-ttu-id="db09f-116">Microsoft. тактов. Canon. Апплисериесофопс</span><span class="sxs-lookup"><span data-stu-id="db09f-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)