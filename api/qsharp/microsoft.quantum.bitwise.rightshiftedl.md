---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Функция Ригхтшифтедл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 03ed69c7151e62b91c4a036e301f99b45ce5ab62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842097"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="ff6e2-102">Функция Ригхтшифтедл</span><span class="sxs-lookup"><span data-stu-id="ff6e2-102">RightShiftedL function</span></span>

<span data-ttu-id="ff6e2-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="ff6e2-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="ff6e2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff6e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff6e2-105">Сдвигает побитовое представление числа вправо на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="ff6e2-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="ff6e2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff6e2-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="ff6e2-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ff6e2-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ff6e2-108">Число, побитовое представление которого должно быть смещено вправо (менее значимое).</span><span class="sxs-lookup"><span data-stu-id="ff6e2-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="ff6e2-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ff6e2-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ff6e2-110">Число битов, на которое `value` будет перемещено право.</span><span class="sxs-lookup"><span data-stu-id="ff6e2-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="ff6e2-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ff6e2-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ff6e2-112">Значение `value` , перемещенное вправо по `amount` битам.</span><span class="sxs-lookup"><span data-stu-id="ff6e2-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff6e2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="ff6e2-113">Remarks</span></span>

<span data-ttu-id="ff6e2-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="ff6e2-114">The following are equivalent:</span></span>

```qsharp
let c = a >>> b;
let c = RightShiftedL(a, b);
```