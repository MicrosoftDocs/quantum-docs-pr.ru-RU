---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Операция Пермутекубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 2fbbe0d99ad1383d77cb08ff6b03bcebd8a1971f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852327"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="e8e68-102">Операция Пермутекубитс</span><span class="sxs-lookup"><span data-stu-id="e8e68-102">PermuteQubits operation</span></span>

<span data-ttu-id="e8e68-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8e68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8e68-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8e68-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8e68-105">Пермутес Кубитс с помощью операции переключения.</span><span class="sxs-lookup"><span data-stu-id="e8e68-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e8e68-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e8e68-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="e8e68-107">упорядочение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e8e68-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e8e68-108">Описание нового порядка Кубитс, где кубит с индексом теперь будет в порядке [i].</span><span class="sxs-lookup"><span data-stu-id="e8e68-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="e8e68-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e8e68-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e8e68-110">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="e8e68-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8e68-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8e68-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="e8e68-112">Пример</span><span class="sxs-lookup"><span data-stu-id="e8e68-112">Example</span></span>

<span data-ttu-id="e8e68-113">При указании Order = [2, 1, 0] и Register $ \кет{\ alpha_0} \кет{\ alpha_1} \кет{\ alpha_2} $ Пермутекубитс изменяет регистр на $ \кет{\ alpha_2} \кет{\ alpha_1} \кет{\ alpha_0} $</span><span class="sxs-lookup"><span data-stu-id="e8e68-113">Given ordering = [2, 1, 0] and register $\ket{\alpha_0} \ket{\alpha_1} \ket{\alpha_2}$, PermuteQubits changes the register into $\ket{\alpha_2} \ket{\alpha_1} \ket{\alpha_0}$</span></span>

```qsharp
// The following two lines are equivalent
PermuteQubits([2, 1, 0], register);
SWAP(register[0], register[2]);
```