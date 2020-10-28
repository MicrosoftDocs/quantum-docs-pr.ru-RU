---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731689"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="9b22a-102">Операция Ассертмостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="9b22a-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="9b22a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9b22a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9b22a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9b22a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9b22a-105">Утверждает, что наиболее значимые кубит регистра кубит, представляющие целое число без знака, находятся в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="9b22a-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="9b22a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9b22a-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="9b22a-107">значение: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="9b22a-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="9b22a-108">Значение самого высокого бита, для которого выполняется утверждение.</span><span class="sxs-lookup"><span data-stu-id="9b22a-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="9b22a-109">число: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9b22a-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9b22a-110">Целое число без знака, для которого установлен наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="9b22a-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b22a-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b22a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9b22a-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b22a-112">Remarks</span></span>

<span data-ttu-id="9b22a-113">Контролируемая версия этой операции не учитывает элементы управления.</span><span class="sxs-lookup"><span data-stu-id="9b22a-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b22a-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="9b22a-114">See Also</span></span>

- [<span data-ttu-id="9b22a-115">Microsoft. тактов. внутренний. Assert</span><span class="sxs-lookup"><span data-stu-id="9b22a-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)