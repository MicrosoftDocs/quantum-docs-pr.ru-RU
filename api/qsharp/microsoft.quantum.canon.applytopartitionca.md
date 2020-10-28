---
uid: Microsoft.Quantum.Canon.ApplyToPartitionCA
title: Операция Апплитопартитионка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionCA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 8ea437a0e25ed43eb745a7740ecd8861ced1350a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717120"
---
# <a name="applytopartitionca-operation"></a><span data-ttu-id="3cf76-102">Операция Апплитопартитионка</span><span class="sxs-lookup"><span data-stu-id="3cf76-102">ApplyToPartitionCA operation</span></span>

<span data-ttu-id="3cf76-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3cf76-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3cf76-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3cf76-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3cf76-105">Применяет пару операций к заданному разделу регистра на две части.</span><span class="sxs-lookup"><span data-stu-id="3cf76-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="3cf76-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="3cf76-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToPartitionCA (op : ((Qubit[], Qubit[]) => Unit is Ctl + Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3cf76-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3cf76-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl--adj"></a><span data-ttu-id="3cf76-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="3cf76-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="3cf76-109">Пара операций, применяемых к заданному разделу.</span><span class="sxs-lookup"><span data-stu-id="3cf76-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="3cf76-110">Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3cf76-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3cf76-111">Число Кубитс от целевого объекта, помещаемых в первую часть секции.</span><span class="sxs-lookup"><span data-stu-id="3cf76-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="3cf76-112">Остальные Кубитс составляют вторую часть секции.</span><span class="sxs-lookup"><span data-stu-id="3cf76-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="3cf76-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3cf76-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3cf76-114">Регистр Кубитс, которые секционированы и управляются данной двумя операциями.</span><span class="sxs-lookup"><span data-stu-id="3cf76-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3cf76-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3cf76-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="3cf76-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="3cf76-116">See Also</span></span>

- [<span data-ttu-id="3cf76-117">Microsoft. тактов. Canon. Апплитопартитион</span><span class="sxs-lookup"><span data-stu-id="3cf76-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)