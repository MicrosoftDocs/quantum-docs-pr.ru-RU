---
uid: Microsoft.Quantum.Math.ModulusL
title: Функция модуля
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842750"
---
# <a name="modulusl-function"></a><span data-ttu-id="2ab35-102">Функция модуля</span><span class="sxs-lookup"><span data-stu-id="2ab35-102">ModulusL function</span></span>

<span data-ttu-id="2ab35-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2ab35-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2ab35-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ab35-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ab35-105">Вычисление канонического ресидуе `value` остатка от деления `modulus` .</span><span class="sxs-lookup"><span data-stu-id="2ab35-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="2ab35-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2ab35-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="2ab35-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2ab35-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2ab35-108">Значение, для которого вычислено ресидуе</span><span class="sxs-lookup"><span data-stu-id="2ab35-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="2ab35-109">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2ab35-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2ab35-110">Модуль, по которому ресидуес принимаются, должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="2ab35-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2ab35-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2ab35-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2ab35-112">Целое число $r $ от 0 до значения `modulus - 1` , `value - r` кратного модулю</span><span class="sxs-lookup"><span data-stu-id="2ab35-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab35-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ab35-113">Remarks</span></span>

<span data-ttu-id="2ab35-114">Эта функция ведет себя иначе, чем оператор `%` в C# и Q #, как в результате, всегда является неотрицательным целым числом от 0 до `modulus - 1` , даже если значение отрицательное.</span><span class="sxs-lookup"><span data-stu-id="2ab35-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>