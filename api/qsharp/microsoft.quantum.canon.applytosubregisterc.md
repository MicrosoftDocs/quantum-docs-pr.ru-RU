---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterC
title: Операция Апплитосубрегистерк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterC
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 52564e64d8cc9cdbeb2626ed8694168b8ed48c22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850465"
---
# <a name="applytosubregisterc-operation"></a><span data-ttu-id="ea63a-102">Операция Апплитосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="ea63a-102">ApplyToSubregisterC operation</span></span>

<span data-ttu-id="ea63a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ea63a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ea63a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea63a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea63a-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="ea63a-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="ea63a-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="ea63a-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[], target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ea63a-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ea63a-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="ea63a-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="ea63a-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ea63a-109">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="ea63a-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="ea63a-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ea63a-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ea63a-111">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="ea63a-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ea63a-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ea63a-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ea63a-113">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="ea63a-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ea63a-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea63a-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ea63a-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="ea63a-115">See Also</span></span>

- [<span data-ttu-id="ea63a-116">Microsoft. тактов. Canon. Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="ea63a-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)