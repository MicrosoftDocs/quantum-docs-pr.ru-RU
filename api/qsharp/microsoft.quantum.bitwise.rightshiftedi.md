---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Функция Ригхтшифтеди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 5c3106eb73178554184cbfb37333c027805c69f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845255"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="cf3c4-102">Функция Ригхтшифтеди</span><span class="sxs-lookup"><span data-stu-id="cf3c4-102">RightShiftedI function</span></span>

<span data-ttu-id="cf3c4-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="cf3c4-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="cf3c4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cf3c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cf3c4-105">Сдвигает побитовое представление числа вправо на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="cf3c4-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="cf3c4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cf3c4-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="cf3c4-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf3c4-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf3c4-108">Число, побитовое представление которого должно быть смещено вправо (менее значимое).</span><span class="sxs-lookup"><span data-stu-id="cf3c4-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="cf3c4-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf3c4-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf3c4-110">Число битов, на которое `value` будет перемещено право.</span><span class="sxs-lookup"><span data-stu-id="cf3c4-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="cf3c4-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf3c4-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf3c4-112">Значение `value` , перемещенное вправо по `amount` битам.</span><span class="sxs-lookup"><span data-stu-id="cf3c4-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf3c4-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="cf3c4-113">Remarks</span></span>

<span data-ttu-id="cf3c4-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="cf3c4-114">The following are equivalent:</span></span>

```qsharp
let c = a >>> b;
let c = RightShiftedI(a, b);
```