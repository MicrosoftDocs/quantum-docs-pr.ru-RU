---
uid: Microsoft.Quantum.Math.ModulusL
title: Функция модуля
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: e7e692059051fde295634c37892ec54e2cf1b095
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733848"
---
# <a name="modulusl-function"></a><span data-ttu-id="b6634-102">Функция модуля</span><span class="sxs-lookup"><span data-stu-id="b6634-102">ModulusL function</span></span>

<span data-ttu-id="b6634-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b6634-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b6634-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6634-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6634-105">Вычисление канонического ресидуе `value` остатка от деления `modulus` .</span><span class="sxs-lookup"><span data-stu-id="b6634-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="b6634-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b6634-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="b6634-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b6634-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b6634-108">Значение, для которого вычислено ресидуе</span><span class="sxs-lookup"><span data-stu-id="b6634-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="b6634-109">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b6634-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b6634-110">Модуль, по которому ресидуес принимаются, должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="b6634-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="b6634-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b6634-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b6634-112">Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю</span><span class="sxs-lookup"><span data-stu-id="b6634-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="b6634-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="b6634-113">Remarks</span></span>

<span data-ttu-id="b6634-114">Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.</span><span class="sxs-lookup"><span data-stu-id="b6634-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>