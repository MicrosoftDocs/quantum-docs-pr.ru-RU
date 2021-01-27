---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Операция Апплитосубрегистерка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9f24c3ca9b152cf9bbf81e59b86f83a0ab459031
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841211"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="cfa34-102">Операция Апплитосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="cfa34-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="cfa34-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cfa34-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cfa34-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cfa34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cfa34-105">Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.</span><span class="sxs-lookup"><span data-stu-id="cfa34-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="cfa34-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="cfa34-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cfa34-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cfa34-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="cfa34-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="cfa34-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cfa34-109">Операция, применяемая к подрегистру.</span><span class="sxs-lookup"><span data-stu-id="cfa34-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="cfa34-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cfa34-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cfa34-111">Массив индексов, указывающий, к какому кубитсу будет применена операция.</span><span class="sxs-lookup"><span data-stu-id="cfa34-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="cfa34-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cfa34-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cfa34-113">Регистрация, в которой действует операция.</span><span class="sxs-lookup"><span data-stu-id="cfa34-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cfa34-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cfa34-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="cfa34-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="cfa34-115">See Also</span></span>

- [<span data-ttu-id="cfa34-116">Microsoft. тактов. Canon. Апплитосубрегистер</span><span class="sxs-lookup"><span data-stu-id="cfa34-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)