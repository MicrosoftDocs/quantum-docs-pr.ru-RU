---
uid: Microsoft.Quantum.Arrays.Swapped
title: Переключенная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 575d6b76e52f198d91ab5557ada8032df491cfa3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850954"
---
# <a name="swapped-function"></a><span data-ttu-id="7a5f2-102">Переключенная функция</span><span class="sxs-lookup"><span data-stu-id="7a5f2-102">Swapped function</span></span>

<span data-ttu-id="7a5f2-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7a5f2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7a5f2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7a5f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7a5f2-105">Применяет перестановку двух элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="7a5f2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7a5f2-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="7a5f2-107">Фирстиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a5f2-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a5f2-108">Индекс первого заменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="7a5f2-109">Секондиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a5f2-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a5f2-110">Индекс второго заменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="7a5f2-111">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="7a5f2-111">arr : 'T[]</span></span>

<span data-ttu-id="7a5f2-112">Массив с элементами для обмена.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="7a5f2-113">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="7a5f2-113">Output : 'T[]</span></span>

<span data-ttu-id="7a5f2-114">Массив с примененным переключением на месте.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="7a5f2-115">Пример</span><span class="sxs-lookup"><span data-stu-id="7a5f2-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="7a5f2-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7a5f2-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7a5f2-117">Е</span><span class="sxs-lookup"><span data-stu-id="7a5f2-117">'T</span></span>

