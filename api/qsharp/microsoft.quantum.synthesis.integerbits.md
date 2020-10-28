---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Функция Интежербитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730665"
---
# <a name="integerbits-function"></a><span data-ttu-id="e2c2f-102">Функция Интежербитс</span><span class="sxs-lookup"><span data-stu-id="e2c2f-102">IntegerBits function</span></span>

<span data-ttu-id="e2c2f-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="e2c2f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="e2c2f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e2c2f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e2c2f-105">Возвращает все позиции, в которых заданы биты целого числа.</span><span class="sxs-lookup"><span data-stu-id="e2c2f-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="e2c2f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e2c2f-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="e2c2f-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e2c2f-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e2c2f-108">Неотрицательное число.</span><span class="sxs-lookup"><span data-stu-id="e2c2f-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="e2c2f-109">Длина: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e2c2f-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e2c2f-110">Число битов в расширении двоичного объекта `value` .</span><span class="sxs-lookup"><span data-stu-id="e2c2f-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="e2c2f-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e2c2f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e2c2f-112">Массив, содержащий все позиции бита (начиная с 0), которые являются 1 в расширении двоичного файла, `value` учитывая все биты до позиции `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="e2c2f-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="e2c2f-113">Все позиции упорядочиваются в массиве по позиции в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="e2c2f-113">All positions are ordered in the array by position in an increasing order.</span></span>