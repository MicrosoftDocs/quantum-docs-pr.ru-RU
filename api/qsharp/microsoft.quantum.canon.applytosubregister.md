---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Операция Апплитосубрегистер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: c9181b8962d36b20f7a9140eb7aaef11aee7faa0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717035"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="1e7b4-102">Операция Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="1e7b4-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="1e7b4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1e7b4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1e7b4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1e7b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1e7b4-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="1e7b4-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1e7b4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1e7b4-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="1e7b4-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="1e7b4-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1e7b4-108">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="1e7b4-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="1e7b4-109">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1e7b4-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1e7b4-110">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="1e7b4-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="1e7b4-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1e7b4-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1e7b4-112">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="1e7b4-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1e7b4-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e7b4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1e7b4-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="1e7b4-114">See Also</span></span>

- [<span data-ttu-id="1e7b4-115">Microsoft. тактов. Canon. Апплитосубрегистера</span><span class="sxs-lookup"><span data-stu-id="1e7b4-115">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="1e7b4-116">Microsoft. тактов. Canon. Апплитосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="1e7b4-116">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="1e7b4-117">Microsoft. тактов. Canon. Апплитосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="1e7b4-117">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)