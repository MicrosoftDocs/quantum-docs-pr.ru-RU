---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Функция Рестриктедтосубрегистерк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f44e9ea4d17dcadc6d3c64941529db819b7f9784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840205"
---
# <a name="restrictedtosubregisterc-function"></a><span data-ttu-id="f0bee-102">Функция Рестриктедтосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="f0bee-102">RestrictedToSubregisterC function</span></span>

<span data-ttu-id="f0bee-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0bee-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0bee-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0bee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0bee-105">Ограничивают операцию массивом индексов регистра, т. е. подрегистром.</span><span class="sxs-lookup"><span data-stu-id="f0bee-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="f0bee-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="f0bee-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="f0bee-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f0bee-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="f0bee-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="f0bee-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f0bee-109">Операция, которая должна быть ограничена подрегистром.</span><span class="sxs-lookup"><span data-stu-id="f0bee-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="f0bee-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f0bee-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f0bee-111">Массив индексов, указывающий, к какому Кубитс операция будет ограничена.</span><span class="sxs-lookup"><span data-stu-id="f0bee-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-ctl"></a><span data-ttu-id="f0bee-112">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  CTL</span><span class="sxs-lookup"><span data-stu-id="f0bee-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="f0bee-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="f0bee-113">See Also</span></span>

- [<span data-ttu-id="f0bee-114">Microsoft. тактов. Canon. Рестриктедтосубрегистер</span><span class="sxs-lookup"><span data-stu-id="f0bee-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)