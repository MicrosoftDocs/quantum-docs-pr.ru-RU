---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Операция Апплитосубрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: be820c87ee19230713d6c3e5681bbe3678040e95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850467"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="e0a96-102">Операция Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="e0a96-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="e0a96-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e0a96-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e0a96-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0a96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0a96-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="e0a96-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e0a96-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0a96-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="e0a96-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="e0a96-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e0a96-108">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="e0a96-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="e0a96-109">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e0a96-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e0a96-110">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="e0a96-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e0a96-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e0a96-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e0a96-112">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="e0a96-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e0a96-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0a96-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="e0a96-114">Пример</span><span class="sxs-lookup"><span data-stu-id="e0a96-114">Example</span></span>

<span data-ttu-id="e0a96-115">Создайте три состояния кубит $ \фрак {1} {\скрт {2} } \кет {0} \_ 2 (\кет {0} \_ 1 \ Сисакет {0} _3 + \кет {1} \_ 1 \ Сисакет {1} _3) $:</span><span class="sxs-lookup"><span data-stu-id="e0a96-115">Create three qubit state $\frac{1}{\sqrt{2}}\ket{0}\_2(\ket{0}\_1\ket{0}_3+\ket{1}\_1\ket{1}_3)$:</span></span>

```qsharp
    using (register = Qubit[3]) {
        ApplyToSubregister(Exp([PauliX,PauliY],PI() / 4.0,_), [1,3], register);
    }
```

## <a name="see-also"></a><span data-ttu-id="e0a96-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e0a96-116">See Also</span></span>

- [<span data-ttu-id="e0a96-117">Microsoft. тактов. Canon. Апплитосубрегистера</span><span class="sxs-lookup"><span data-stu-id="e0a96-117">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="e0a96-118">Microsoft. тактов. Canon. Апплитосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="e0a96-118">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="e0a96-119">Microsoft. тактов. Canon. Апплитосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="e0a96-119">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)