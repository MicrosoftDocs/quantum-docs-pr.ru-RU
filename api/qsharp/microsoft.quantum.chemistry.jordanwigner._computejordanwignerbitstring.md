---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Функция _ComputeJordanWignerBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203949"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="d11d9-102">Функция _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="d11d9-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="d11d9-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d11d9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d11d9-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d11d9-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d11d9-105">Вычисление Z-компонента Иордания — Вигнер строки между фермион индексами в операторе фермионик с четным числом операторов создания или аннихилатион.</span><span class="sxs-lookup"><span data-stu-id="d11d9-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="d11d9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d11d9-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="d11d9-107">Нфермионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d11d9-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d11d9-108">Число фермионс в системе.</span><span class="sxs-lookup"><span data-stu-id="d11d9-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="d11d9-109">Идксфермионс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d11d9-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d11d9-110">Индексы операторов фермионик.</span><span class="sxs-lookup"><span data-stu-id="d11d9-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d11d9-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d11d9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d11d9-112">Битстринг `Bool[]` , `true` `PauliZ` к которому следует применить.</span><span class="sxs-lookup"><span data-stu-id="d11d9-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>