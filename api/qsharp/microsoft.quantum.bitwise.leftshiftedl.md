---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Функция Лефтшифтедл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 00d4f9151c620e044074930933ea2912b52534ed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219674"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="4e561-102">Функция Лефтшифтедл</span><span class="sxs-lookup"><span data-stu-id="4e561-102">LeftShiftedL function</span></span>

<span data-ttu-id="4e561-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="4e561-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="4e561-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e561-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e561-105">Сдвигает побитовое представление числа влево на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="4e561-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="4e561-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4e561-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="4e561-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4e561-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4e561-108">Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).</span><span class="sxs-lookup"><span data-stu-id="4e561-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="4e561-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4e561-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4e561-110">Число битов, на которое `value` будет перемещен влево.</span><span class="sxs-lookup"><span data-stu-id="4e561-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="4e561-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4e561-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4e561-112">Значение `value` , смещенное влево на `amount` биты.</span><span class="sxs-lookup"><span data-stu-id="4e561-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e561-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e561-113">Remarks</span></span>

<span data-ttu-id="4e561-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="4e561-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```