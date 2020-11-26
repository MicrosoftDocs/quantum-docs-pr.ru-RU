---
uid: Microsoft.Quantum.Arrays.Swapped
title: Переключенная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 173fb32b5a41ce054f19548a7fcca18c11c4c4cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220133"
---
# <a name="swapped-function"></a><span data-ttu-id="2e876-102">Переключенная функция</span><span class="sxs-lookup"><span data-stu-id="2e876-102">Swapped function</span></span>

<span data-ttu-id="2e876-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e876-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e876-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e876-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e876-105">Применяет перестановку двух элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="2e876-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="2e876-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2e876-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="2e876-107">Фирстиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2e876-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2e876-108">Индекс первого заменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="2e876-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="2e876-109">Секондиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2e876-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2e876-110">Индекс второго заменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="2e876-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="2e876-111">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="2e876-111">arr : 'T[]</span></span>

<span data-ttu-id="2e876-112">Массив с элементами для обмена.</span><span class="sxs-lookup"><span data-stu-id="2e876-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="2e876-113">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="2e876-113">Output : 'T[]</span></span>

<span data-ttu-id="2e876-114">Массив с примененным переключением на месте.</span><span class="sxs-lookup"><span data-stu-id="2e876-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="2e876-115">Пример</span><span class="sxs-lookup"><span data-stu-id="2e876-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="2e876-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2e876-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e876-117">Е</span><span class="sxs-lookup"><span data-stu-id="2e876-117">'T</span></span>

