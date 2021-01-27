---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Операция Апплитопартитиона
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: f8f773e9fc3c18467185f9717a235649be8b385a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841294"
---
# <a name="applytopartitiona-operation"></a><span data-ttu-id="f6a59-102">Операция Апплитопартитиона</span><span class="sxs-lookup"><span data-stu-id="f6a59-102">ApplyToPartitionA operation</span></span>

<span data-ttu-id="f6a59-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f6a59-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f6a59-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6a59-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6a59-105">Применяет пару операций к заданному разделу регистра на две части.</span><span class="sxs-lookup"><span data-stu-id="f6a59-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="f6a59-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="f6a59-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f6a59-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f6a59-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="f6a59-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой</span><span class="sxs-lookup"><span data-stu-id="f6a59-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f6a59-109">Пара операций, применяемых к заданному разделу.</span><span class="sxs-lookup"><span data-stu-id="f6a59-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="f6a59-110">Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6a59-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6a59-111">Число Кубитс от целевого объекта, помещаемых в первую часть секции.</span><span class="sxs-lookup"><span data-stu-id="f6a59-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="f6a59-112">Остальные Кубитс составляют вторую часть секции.</span><span class="sxs-lookup"><span data-stu-id="f6a59-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f6a59-113">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f6a59-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f6a59-114">Регистр Кубитс, которые секционированы и управляются данной двумя операциями.</span><span class="sxs-lookup"><span data-stu-id="f6a59-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f6a59-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6a59-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f6a59-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="f6a59-116">See Also</span></span>

- [<span data-ttu-id="f6a59-117">Microsoft. тактов. Canon. Апплитопартитион</span><span class="sxs-lookup"><span data-stu-id="f6a59-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)