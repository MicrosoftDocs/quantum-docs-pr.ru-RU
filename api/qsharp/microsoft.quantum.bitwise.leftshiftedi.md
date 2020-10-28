---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Функция Лефтшифтеди
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729880"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="0dbb2-102">Функция Лефтшифтеди</span><span class="sxs-lookup"><span data-stu-id="0dbb2-102">LeftShiftedI function</span></span>

<span data-ttu-id="0dbb2-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="0dbb2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0dbb2-105">Сдвигает побитовое представление числа влево на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="0dbb2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0dbb2-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="0dbb2-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dbb2-108">Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="0dbb2-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dbb2-110">Число битов, на которое `value` будет перемещен влево.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="0dbb2-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dbb2-112">Значение `value` , смещенное влево на `amount` биты.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dbb2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="0dbb2-113">Remarks</span></span>

<span data-ttu-id="0dbb2-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="0dbb2-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```