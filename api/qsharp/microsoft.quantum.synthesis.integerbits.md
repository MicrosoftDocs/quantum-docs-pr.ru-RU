---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Функция Интежербитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: d6566716f5a63c090668d9582b7b000c16d1f6a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231098"
---
# <a name="integerbits-function"></a><span data-ttu-id="ad088-102">Функция Интежербитс</span><span class="sxs-lookup"><span data-stu-id="ad088-102">IntegerBits function</span></span>

<span data-ttu-id="ad088-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ad088-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ad088-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad088-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad088-105">Возвращает все позиции, в которых заданы биты целого числа.</span><span class="sxs-lookup"><span data-stu-id="ad088-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="ad088-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad088-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="ad088-107">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ad088-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ad088-108">Неотрицательное число.</span><span class="sxs-lookup"><span data-stu-id="ad088-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="ad088-109">Длина: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ad088-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ad088-110">Число битов в расширении двоичного объекта `value` .</span><span class="sxs-lookup"><span data-stu-id="ad088-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="ad088-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ad088-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ad088-112">Массив, содержащий все позиции бита (начиная с 0), которые являются 1 в расширении двоичного файла, `value` учитывая все биты до позиции `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="ad088-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="ad088-113">Все позиции упорядочиваются в массиве по позиции в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="ad088-113">All positions are ordered in the array by position in an increasing order.</span></span>