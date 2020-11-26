---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Операция Пермутекубитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: deb5fa5b0bc0509c957e01bf22e491ad3e2214f3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205612"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="7ef9e-102">Операция Пермутекубитс</span><span class="sxs-lookup"><span data-stu-id="7ef9e-102">PermuteQubits operation</span></span>

<span data-ttu-id="7ef9e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ef9e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ef9e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ef9e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ef9e-105">Пермутес Кубитс с помощью операции переключения.</span><span class="sxs-lookup"><span data-stu-id="7ef9e-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7ef9e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7ef9e-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="7ef9e-107">упорядочение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7ef9e-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="7ef9e-108">Описание нового порядка Кубитс, где кубит с индексом теперь будет в порядке [i].</span><span class="sxs-lookup"><span data-stu-id="7ef9e-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="7ef9e-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7ef9e-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7ef9e-110">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="7ef9e-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7ef9e-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7ef9e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

