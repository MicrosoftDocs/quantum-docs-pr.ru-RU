---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: Функция Рестриктедтосубрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: c5a6bbe16d2f6a317f6ed6f258077095465995f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840230"
---
# <a name="restrictedtosubregister-function"></a><span data-ttu-id="720c9-102">Функция Рестриктедтосубрегистер</span><span class="sxs-lookup"><span data-stu-id="720c9-102">RestrictedToSubregister function</span></span>

<span data-ttu-id="720c9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="720c9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="720c9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="720c9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="720c9-105">Ограничивают операцию массивом индексов регистра, т. е. подрегистром.</span><span class="sxs-lookup"><span data-stu-id="720c9-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a><span data-ttu-id="720c9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="720c9-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="720c9-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="720c9-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="720c9-108">Операция, которая должна быть ограничена подрегистром.</span><span class="sxs-lookup"><span data-stu-id="720c9-108">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="720c9-109">идксс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="720c9-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="720c9-110">Массив индексов, указывающий, к какому Кубитс операция будет ограничена.</span><span class="sxs-lookup"><span data-stu-id="720c9-110">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit"></a><span data-ttu-id="720c9-111">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="720c9-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 



## <a name="see-also"></a><span data-ttu-id="720c9-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="720c9-112">See Also</span></span>

- [<span data-ttu-id="720c9-113">Microsoft. тактов. Canon. Рестриктедтосубрегистера</span><span class="sxs-lookup"><span data-stu-id="720c9-113">Microsoft.Quantum.Canon.RestrictedToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [<span data-ttu-id="720c9-114">Microsoft. тактов. Canon. Рестриктедтосубрегистерк</span><span class="sxs-lookup"><span data-stu-id="720c9-114">Microsoft.Quantum.Canon.RestrictedToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [<span data-ttu-id="720c9-115">Microsoft. тактов. Canon. Рестриктедтосубрегистерка</span><span class="sxs-lookup"><span data-stu-id="720c9-115">Microsoft.Quantum.Canon.RestrictedToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)