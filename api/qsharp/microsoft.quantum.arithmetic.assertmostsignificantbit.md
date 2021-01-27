---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843421"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="cbaf9-102">Операция Ассертмостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="cbaf9-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="cbaf9-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="cbaf9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="cbaf9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbaf9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbaf9-105">Утверждает, что наиболее значимые кубит регистра кубит, представляющие целое число без знака, находятся в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="cbaf9-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cbaf9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cbaf9-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="cbaf9-107">значение: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="cbaf9-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="cbaf9-108">Значение самого высокого бита, для которого выполняется утверждение.</span><span class="sxs-lookup"><span data-stu-id="cbaf9-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="cbaf9-109">число: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cbaf9-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cbaf9-110">Целое число без знака, для которого установлен наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="cbaf9-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbaf9-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbaf9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cbaf9-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbaf9-112">Remarks</span></span>

<span data-ttu-id="cbaf9-113">Контролируемая версия этой операции не учитывает элементы управления.</span><span class="sxs-lookup"><span data-stu-id="cbaf9-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbaf9-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="cbaf9-114">See Also</span></span>

- [<span data-ttu-id="cbaf9-115">Microsoft. тактов. внутренний. Assert</span><span class="sxs-lookup"><span data-stu-id="cbaf9-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)