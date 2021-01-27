---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Операция Апплитосубрегистера
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7a5ae78edcda363f21cadaaed5cb273d35cb60cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841226"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="77169-102">Операция Апплитосубрегистера</span><span class="sxs-lookup"><span data-stu-id="77169-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="77169-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77169-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77169-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77169-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77169-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="77169-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="77169-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="77169-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="77169-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="77169-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="77169-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="77169-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="77169-109">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="77169-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="77169-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="77169-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="77169-111">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="77169-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="77169-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="77169-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="77169-113">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="77169-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77169-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77169-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="77169-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="77169-115">See Also</span></span>

- [<span data-ttu-id="77169-116">Microsoft. тактов. Canon. Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="77169-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)