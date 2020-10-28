---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Операция Апплитосубрегистера
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: e0c546b768320ce43e7b44242d15838194e1089d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717022"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="697fe-102">Операция Апплитосубрегистера</span><span class="sxs-lookup"><span data-stu-id="697fe-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="697fe-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="697fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="697fe-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="697fe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="697fe-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="697fe-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="697fe-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="697fe-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="697fe-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="697fe-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="697fe-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="697fe-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="697fe-109">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="697fe-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="697fe-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="697fe-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="697fe-111">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="697fe-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="697fe-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="697fe-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="697fe-113">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="697fe-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="697fe-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="697fe-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="697fe-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="697fe-115">See Also</span></span>

- [<span data-ttu-id="697fe-116">Microsoft. тактов. Canon. Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="697fe-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)