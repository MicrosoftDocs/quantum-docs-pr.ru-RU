---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Функция Лефтшифтедл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842140"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="56efb-102">Функция Лефтшифтедл</span><span class="sxs-lookup"><span data-stu-id="56efb-102">LeftShiftedL function</span></span>

<span data-ttu-id="56efb-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="56efb-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="56efb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56efb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56efb-105">Сдвигает побитовое представление числа влево на заданное число битов.</span><span class="sxs-lookup"><span data-stu-id="56efb-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="56efb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="56efb-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="56efb-107">значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="56efb-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="56efb-108">Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).</span><span class="sxs-lookup"><span data-stu-id="56efb-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="56efb-109">сумма: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56efb-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56efb-110">Число битов, на которое `value` будет перемещен влево.</span><span class="sxs-lookup"><span data-stu-id="56efb-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="56efb-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="56efb-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="56efb-112">Значение `value` , смещенное влево на `amount` биты.</span><span class="sxs-lookup"><span data-stu-id="56efb-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="56efb-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="56efb-113">Remarks</span></span>

<span data-ttu-id="56efb-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="56efb-114">The following are equivalent:</span></span>

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```