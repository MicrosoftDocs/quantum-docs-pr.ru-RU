---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Функция Ригхтшифтеди
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b0ca7d3cb84c58429e9b3a29893a6140a717006b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729824"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="0dfa2-102">Функция Ригхтшифтеди</span><span class="sxs-lookup"><span data-stu-id="0dfa2-102">RightShiftedI function</span></span>

<span data-ttu-id="0dfa2-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="0dfa2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0dfa2-105">Сдвигает побитовое представление числа вправо на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="0dfa2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0dfa2-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="0dfa2-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dfa2-108">Число, побитовое представление которого должно быть смещено вправо (менее значимое).</span><span class="sxs-lookup"><span data-stu-id="0dfa2-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="0dfa2-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dfa2-110">Число битов, на которое `value` будет перемещено право.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="0dfa2-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dfa2-112">Значение `value` , перемещенное вправо по `amount` битам.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfa2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="0dfa2-113">Remarks</span></span>

<span data-ttu-id="0dfa2-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="0dfa2-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```