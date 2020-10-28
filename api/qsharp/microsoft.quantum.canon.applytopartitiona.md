---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Операция Апплитопартитиона
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 6ff3bf8b5a4344ee5a7a054c6285a5492260068d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717133"
---
# <a name="applytopartitiona-operation"></a><span data-ttu-id="84836-102">Операция Апплитопартитиона</span><span class="sxs-lookup"><span data-stu-id="84836-102">ApplyToPartitionA operation</span></span>

<span data-ttu-id="84836-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84836-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84836-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84836-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84836-105">Применяет пару операций к заданному разделу регистра на две части.</span><span class="sxs-lookup"><span data-stu-id="84836-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="84836-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="84836-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="84836-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="84836-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj"></a><span data-ttu-id="84836-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="84836-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="84836-109">Пара операций, применяемых к заданному разделу.</span><span class="sxs-lookup"><span data-stu-id="84836-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="84836-110">Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="84836-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="84836-111">Число Кубитс от целевого объекта, помещаемых в первую часть секции.</span><span class="sxs-lookup"><span data-stu-id="84836-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="84836-112">Остальные Кубитс составляют вторую часть секции.</span><span class="sxs-lookup"><span data-stu-id="84836-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="84836-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="84836-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="84836-114">Регистр Кубитс, которые секционированы и управляются данной двумя операциями.</span><span class="sxs-lookup"><span data-stu-id="84836-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="84836-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84836-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="84836-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="84836-116">See Also</span></span>

- [<span data-ttu-id="84836-117">Microsoft. тактов. Canon. Апплитопартитион</span><span class="sxs-lookup"><span data-stu-id="84836-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)