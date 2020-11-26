---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Операция Ассертмостсигнификантбит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223788"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="406b5-102">Операция Ассертмостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="406b5-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="406b5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="406b5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="406b5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="406b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="406b5-105">Утверждает, что наиболее значимые кубит регистра кубит, представляющие целое число без знака, находятся в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="406b5-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="406b5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="406b5-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="406b5-107">значение: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="406b5-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="406b5-108">Значение самого высокого бита, для которого выполняется утверждение.</span><span class="sxs-lookup"><span data-stu-id="406b5-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="406b5-109">число: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="406b5-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="406b5-110">Целое число без знака, для которого установлен наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="406b5-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="406b5-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="406b5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="406b5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="406b5-112">Remarks</span></span>

<span data-ttu-id="406b5-113">Контролируемая версия этой операции не учитывает элементы управления.</span><span class="sxs-lookup"><span data-stu-id="406b5-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="406b5-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="406b5-114">See Also</span></span>

- [<span data-ttu-id="406b5-115">Microsoft. тактов. внутренний. Assert</span><span class="sxs-lookup"><span data-stu-id="406b5-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)