---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847292"
---
# <a name="modulusi-function"></a><span data-ttu-id="64957-102">Функция Модулуси</span><span class="sxs-lookup"><span data-stu-id="64957-102">ModulusI function</span></span>

<span data-ttu-id="64957-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="64957-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="64957-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64957-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64957-105">Вычисление канонического ресидуе `value` остатка от деления `modulus` .</span><span class="sxs-lookup"><span data-stu-id="64957-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="64957-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="64957-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="64957-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64957-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64957-108">Значение, для которого вычислено ресидуе</span><span class="sxs-lookup"><span data-stu-id="64957-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="64957-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64957-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64957-110">Модуль, по которому ресидуес принимаются, должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="64957-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="64957-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64957-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64957-112">Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю</span><span class="sxs-lookup"><span data-stu-id="64957-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="64957-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="64957-113">Remarks</span></span>

<span data-ttu-id="64957-114">Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является неотрицательным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.</span><span class="sxs-lookup"><span data-stu-id="64957-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>