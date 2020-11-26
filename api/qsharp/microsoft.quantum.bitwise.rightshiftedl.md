---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Функция Ригхтшифтедл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219521"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="6e362-102">Функция Ригхтшифтедл</span><span class="sxs-lookup"><span data-stu-id="6e362-102">RightShiftedL function</span></span>

<span data-ttu-id="6e362-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="6e362-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="6e362-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e362-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e362-105">Сдвигает побитовое представление числа вправо на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="6e362-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="6e362-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6e362-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="6e362-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6e362-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6e362-108">Число, побитовое представление которого должно быть смещено вправо (менее значимое).</span><span class="sxs-lookup"><span data-stu-id="6e362-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="6e362-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6e362-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6e362-110">Число битов, на которое `value` будет перемещено право.</span><span class="sxs-lookup"><span data-stu-id="6e362-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="6e362-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6e362-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6e362-112">Значение `value` , перемещенное вправо по `amount` битам.</span><span class="sxs-lookup"><span data-stu-id="6e362-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e362-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e362-113">Remarks</span></span>

<span data-ttu-id="6e362-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="6e362-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```