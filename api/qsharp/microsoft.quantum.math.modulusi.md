---
uid: Microsoft.Quantum.Math.ModulusI
title: Функция Модулуси
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 3f698a00b2c8d94b7cb3cca4f1721c659918f4a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732697"
---
# <a name="modulusi-function"></a><span data-ttu-id="bcb28-102">Функция Модулуси</span><span class="sxs-lookup"><span data-stu-id="bcb28-102">ModulusI function</span></span>

<span data-ttu-id="bcb28-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bcb28-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bcb28-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bcb28-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bcb28-105">Вычисление канонического ресидуе `value` остатка от деления `modulus` .</span><span class="sxs-lookup"><span data-stu-id="bcb28-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="bcb28-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bcb28-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="bcb28-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bcb28-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bcb28-108">Значение, для которого вычислено ресидуе</span><span class="sxs-lookup"><span data-stu-id="bcb28-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="bcb28-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bcb28-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bcb28-110">Модуль, по которому ресидуес принимаются, должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="bcb28-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="bcb28-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bcb28-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bcb28-112">Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю</span><span class="sxs-lookup"><span data-stu-id="bcb28-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb28-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="bcb28-113">Remarks</span></span>

<span data-ttu-id="bcb28-114">Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является положительным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.</span><span class="sxs-lookup"><span data-stu-id="bcb28-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>