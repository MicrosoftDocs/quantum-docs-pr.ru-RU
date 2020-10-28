---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Операция Апплитопартитионк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717119"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="c266c-102">Операция Апплитопартитионк</span><span class="sxs-lookup"><span data-stu-id="c266c-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="c266c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c266c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c266c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c266c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c266c-105">Применяет пару операций к заданному разделу регистра на две части.</span><span class="sxs-lookup"><span data-stu-id="c266c-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="c266c-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="c266c-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c266c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c266c-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="c266c-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = CTL [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="c266c-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="c266c-109">Пара операций, применяемых к заданному разделу.</span><span class="sxs-lookup"><span data-stu-id="c266c-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="c266c-110">Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c266c-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c266c-111">Число Кубитс от целевого объекта, помещаемых в первую часть секции.</span><span class="sxs-lookup"><span data-stu-id="c266c-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="c266c-112">Остальные Кубитс составляют вторую часть секции.</span><span class="sxs-lookup"><span data-stu-id="c266c-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c266c-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c266c-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c266c-114">Регистр Кубитс, которые секционированы и управляются данной двумя операциями.</span><span class="sxs-lookup"><span data-stu-id="c266c-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c266c-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c266c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c266c-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c266c-116">See Also</span></span>

- [<span data-ttu-id="c266c-117">Microsoft. тактов. Canon. Апплитопартитион</span><span class="sxs-lookup"><span data-stu-id="c266c-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)