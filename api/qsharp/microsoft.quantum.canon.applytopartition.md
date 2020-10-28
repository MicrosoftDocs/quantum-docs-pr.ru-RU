---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Операция Апплитопартитион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: c1f43e7936fc1c18fb665388e9892dc3b74cdd05
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717147"
---
# <a name="applytopartition-operation"></a><span data-ttu-id="e1081-102">Операция Апплитопартитион</span><span class="sxs-lookup"><span data-stu-id="e1081-102">ApplyToPartition operation</span></span>

<span data-ttu-id="e1081-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e1081-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e1081-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1081-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1081-105">Применяет пару операций к заданному разделу регистра на две части.</span><span class="sxs-lookup"><span data-stu-id="e1081-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e1081-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e1081-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="e1081-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="e1081-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e1081-108">Пара операций, применяемых к заданному разделу.</span><span class="sxs-lookup"><span data-stu-id="e1081-108">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="e1081-109">Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e1081-109">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e1081-110">Число Кубитс от целевого объекта, помещаемых в первую часть секции.</span><span class="sxs-lookup"><span data-stu-id="e1081-110">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="e1081-111">Остальные Кубитс составляют вторую часть секции.</span><span class="sxs-lookup"><span data-stu-id="e1081-111">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e1081-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e1081-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e1081-113">Регистр Кубитс, которые секционированы и управляются данной двумя операциями.</span><span class="sxs-lookup"><span data-stu-id="e1081-113">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1081-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1081-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e1081-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="e1081-115">See Also</span></span>

- [<span data-ttu-id="e1081-116">Microsoft. тактов. Canon. Апплитопартитиона</span><span class="sxs-lookup"><span data-stu-id="e1081-116">Microsoft.Quantum.Canon.ApplyToPartitionA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [<span data-ttu-id="e1081-117">Microsoft. тактов. Canon. Апплитопартитионк</span><span class="sxs-lookup"><span data-stu-id="e1081-117">Microsoft.Quantum.Canon.ApplyToPartitionC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [<span data-ttu-id="e1081-118">Microsoft. тактов. Canon. Апплитопартитионка</span><span class="sxs-lookup"><span data-stu-id="e1081-118">Microsoft.Quantum.Canon.ApplyToPartitionCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)