---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Функция Рестриктедтосубрегистерка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9b1c8a6d1c843fb0533af16aafc4b3ca2ba2f0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852176"
---
# <a name="restrictedtosubregisterca-function"></a><span data-ttu-id="06c88-102">Функция Рестриктедтосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="06c88-102">RestrictedToSubregisterCA function</span></span>

<span data-ttu-id="06c88-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="06c88-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="06c88-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06c88-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06c88-105">Ограничивают операцию массивом индексов регистра, т. е. подрегистром.</span><span class="sxs-lookup"><span data-stu-id="06c88-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="06c88-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="06c88-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="06c88-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="06c88-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="06c88-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="06c88-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="06c88-109">Операция, которая должна быть ограничена подрегистром.</span><span class="sxs-lookup"><span data-stu-id="06c88-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="06c88-110">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="06c88-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="06c88-111">Массив индексов, указывающий, к какому Кубитс операция будет ограничена.</span><span class="sxs-lookup"><span data-stu-id="06c88-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="06c88-112">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="06c88-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="06c88-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="06c88-113">See Also</span></span>

- [<span data-ttu-id="06c88-114">Microsoft. тактов. Canon. Рестриктедтосубрегистер</span><span class="sxs-lookup"><span data-stu-id="06c88-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)