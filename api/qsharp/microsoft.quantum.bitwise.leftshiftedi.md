---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Функция Лефтшифтеди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3f551bdba5c8e2a1456838769e4cee0660d0f969
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845307"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="945d5-102">Функция Лефтшифтеди</span><span class="sxs-lookup"><span data-stu-id="945d5-102">LeftShiftedI function</span></span>

<span data-ttu-id="945d5-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="945d5-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="945d5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="945d5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="945d5-105">Сдвигает побитовое представление числа влево на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="945d5-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="945d5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="945d5-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="945d5-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="945d5-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="945d5-108">Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).</span><span class="sxs-lookup"><span data-stu-id="945d5-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="945d5-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="945d5-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="945d5-110">Число битов, на которое `value` будет перемещен влево.</span><span class="sxs-lookup"><span data-stu-id="945d5-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="945d5-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="945d5-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="945d5-112">Значение `value` , смещенное влево на `amount` биты.</span><span class="sxs-lookup"><span data-stu-id="945d5-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="945d5-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="945d5-113">Remarks</span></span>

<span data-ttu-id="945d5-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="945d5-114">The following are equivalent:</span></span>

```qsharp
let c = a <<< b;
let c = LeftShiftedI(a, b);
```