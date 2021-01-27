---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Функция _ComputeJordanWignerBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839525"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="611d1-102">Функция _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="611d1-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="611d1-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="611d1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="611d1-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="611d1-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="611d1-105">Вычисление Z-компонента Иордания — Вигнер строки между фермион индексами в операторе фермионик с четным числом операторов создания или аннихилатион.</span><span class="sxs-lookup"><span data-stu-id="611d1-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="611d1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="611d1-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="611d1-107">Нфермионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="611d1-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="611d1-108">Число фермионс в системе.</span><span class="sxs-lookup"><span data-stu-id="611d1-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="611d1-109">Идксфермионс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="611d1-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="611d1-110">Индексы операторов фермионик.</span><span class="sxs-lookup"><span data-stu-id="611d1-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="611d1-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="611d1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="611d1-112">Битстринг `Bool[]` , `true` `PauliZ` к которому следует применить.</span><span class="sxs-lookup"><span data-stu-id="611d1-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>

## <a name="example"></a><span data-ttu-id="611d1-113">Пример</span><span class="sxs-lookup"><span data-stu-id="611d1-113">Example</span></span>

<span data-ttu-id="611d1-114">Let Битстринг = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); Битстринг имеет значение [false, false, false, true, true, true, false].</span><span class="sxs-lookup"><span data-stu-id="611d1-114">let bitString = _ComputeJordanWignerBitString(6, [0,1,2,6]) ; // bitString is [false, false, false ,true, true, true, false].</span></span>