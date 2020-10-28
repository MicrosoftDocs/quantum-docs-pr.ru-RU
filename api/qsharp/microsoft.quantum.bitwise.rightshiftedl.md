---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Функция Ригхтшифтедл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 2929ba58b636847257391930e1019769fd2c2580
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729817"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="fa30b-102">Функция Ригхтшифтедл</span><span class="sxs-lookup"><span data-stu-id="fa30b-102">RightShiftedL function</span></span>

<span data-ttu-id="fa30b-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="fa30b-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="fa30b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fa30b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fa30b-105">Сдвигает побитовое представление числа вправо на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="fa30b-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="fa30b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fa30b-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="fa30b-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fa30b-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fa30b-108">Число, побитовое представление которого должно быть смещено вправо (менее значимое).</span><span class="sxs-lookup"><span data-stu-id="fa30b-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="fa30b-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fa30b-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fa30b-110">Число битов, на которое `value` будет перемещено право.</span><span class="sxs-lookup"><span data-stu-id="fa30b-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="fa30b-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fa30b-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fa30b-112">Значение `value` , перемещенное вправо по `amount` битам.</span><span class="sxs-lookup"><span data-stu-id="fa30b-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa30b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa30b-113">Remarks</span></span>

<span data-ttu-id="fa30b-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="fa30b-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```