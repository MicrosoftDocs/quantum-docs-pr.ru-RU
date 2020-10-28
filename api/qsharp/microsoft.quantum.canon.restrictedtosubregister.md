---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: Функция Рестриктедтосубрегистер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: a8b599035de6fede10bdaf8cef17f2124a59f064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715538"
---
# <a name="restrictedtosubregister-function"></a><span data-ttu-id="25a5a-102">Функция Рестриктедтосубрегистер</span><span class="sxs-lookup"><span data-stu-id="25a5a-102">RestrictedToSubregister function</span></span>

<span data-ttu-id="25a5a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="25a5a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="25a5a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25a5a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25a5a-105">Ограничивают операцию массивом индексов регистра, т. е. подрегистром.</span><span class="sxs-lookup"><span data-stu-id="25a5a-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a><span data-ttu-id="25a5a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="25a5a-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="25a5a-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="25a5a-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="25a5a-108">Операция, которая должна быть ограничена подрегистром.</span><span class="sxs-lookup"><span data-stu-id="25a5a-108">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="25a5a-109">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25a5a-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25a5a-110">Массив индексов, указывающий, к какому Кубитс операция будет ограничена.</span><span class="sxs-lookup"><span data-stu-id="25a5a-110">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit"></a><span data-ttu-id="25a5a-111">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="25a5a-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 



## <a name="see-also"></a><span data-ttu-id="25a5a-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="25a5a-112">See Also</span></span>

- [<span data-ttu-id="25a5a-113">Microsoft. тактов. Canon. Рестриктедтосубрегистера</span><span class="sxs-lookup"><span data-stu-id="25a5a-113">Microsoft.Quantum.Canon.RestrictedToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [<span data-ttu-id="25a5a-114">Microsoft. тактов. Canon. Рестриктедтосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="25a5a-114">Microsoft.Quantum.Canon.RestrictedToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [<span data-ttu-id="25a5a-115">Microsoft. тактов. Canon. Рестриктедтосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="25a5a-115">Microsoft.Quantum.Canon.RestrictedToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)