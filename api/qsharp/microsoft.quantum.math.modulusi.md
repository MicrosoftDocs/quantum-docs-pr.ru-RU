---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6bbb3877b93e1fc6b38f85a716ba617311c7cfba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227783"
---
# <a name="modulusi-function"></a><span data-ttu-id="51c1a-102">Функция Модулуси</span><span class="sxs-lookup"><span data-stu-id="51c1a-102">ModulusI function</span></span>

<span data-ttu-id="51c1a-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="51c1a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="51c1a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51c1a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51c1a-105">Вычисление канонического ресидуе `value` остатка от деления `modulus` .</span><span class="sxs-lookup"><span data-stu-id="51c1a-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="51c1a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="51c1a-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="51c1a-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51c1a-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51c1a-108">Значение, для которого вычислено ресидуе</span><span class="sxs-lookup"><span data-stu-id="51c1a-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="51c1a-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51c1a-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51c1a-110">Модуль, по которому ресидуес принимаются, должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="51c1a-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="51c1a-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51c1a-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51c1a-112">Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю</span><span class="sxs-lookup"><span data-stu-id="51c1a-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="51c1a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51c1a-113">Remarks</span></span>

<span data-ttu-id="51c1a-114">Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.</span><span class="sxs-lookup"><span data-stu-id="51c1a-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>