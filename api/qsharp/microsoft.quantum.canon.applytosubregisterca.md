---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Операция Апплитосубрегистерка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 3eb210debf8980f057ed150f647d545f68734459
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716993"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="0691f-102">Операция Апплитосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="0691f-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="0691f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0691f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0691f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0691f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0691f-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="0691f-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="0691f-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="0691f-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0691f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0691f-107">Input</span></span>

### <a name="op--qubit--unit-ctl--adj"></a><span data-ttu-id="0691f-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]> = [единица](xref:microsoft.quantum.lang-ref.unit) CTL + года</span><span class="sxs-lookup"><span data-stu-id="0691f-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="0691f-109">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="0691f-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="0691f-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0691f-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0691f-111">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="0691f-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="0691f-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0691f-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0691f-113">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="0691f-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0691f-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0691f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0691f-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="0691f-115">See Also</span></span>

- [<span data-ttu-id="0691f-116">Microsoft. тактов. Canon. Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="0691f-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)