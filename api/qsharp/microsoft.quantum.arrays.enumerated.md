---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Функция Enumerate
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848129"
---
# <a name="enumerated-function"></a><span data-ttu-id="fc60c-102">Функция Enumerate</span><span class="sxs-lookup"><span data-stu-id="fc60c-102">Enumerated function</span></span>

<span data-ttu-id="fc60c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fc60c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fc60c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc60c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc60c-105">При наличии массива возвращает новый массив, содержащий элементы исходного массива вместе с индексами каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="fc60c-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="fc60c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fc60c-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="fc60c-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="fc60c-107">array : 'TElement[]</span></span>

<span data-ttu-id="fc60c-108">Массив, элементы которого необходимо перечислить.</span><span class="sxs-lookup"><span data-stu-id="fc60c-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="fc60c-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement ') []</span><span class="sxs-lookup"><span data-stu-id="fc60c-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="fc60c-110">Новый массив, содержащий элементы исходного массива вместе с их индексами.</span><span class="sxs-lookup"><span data-stu-id="fc60c-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fc60c-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fc60c-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="fc60c-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="fc60c-112">'TElement</span></span>

<span data-ttu-id="fc60c-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="fc60c-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="fc60c-114">Пример</span><span class="sxs-lookup"><span data-stu-id="fc60c-114">Example</span></span>

<span data-ttu-id="fc60c-115">Следующие `for` циклы эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="fc60c-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```