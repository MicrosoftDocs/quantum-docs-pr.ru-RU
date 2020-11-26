---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Функция Enumerate
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221425"
---
# <a name="enumerated-function"></a><span data-ttu-id="dcf9b-102">Функция Enumerate</span><span class="sxs-lookup"><span data-stu-id="dcf9b-102">Enumerated function</span></span>

<span data-ttu-id="dcf9b-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dcf9b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dcf9b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dcf9b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dcf9b-105">При наличии массива возвращает новый массив, содержащий элементы исходного массива вместе с индексами каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="dcf9b-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="dcf9b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dcf9b-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="dcf9b-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="dcf9b-107">array : 'TElement[]</span></span>

<span data-ttu-id="dcf9b-108">Массив, элементы которого необходимо перечислить.</span><span class="sxs-lookup"><span data-stu-id="dcf9b-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="dcf9b-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement ') []</span><span class="sxs-lookup"><span data-stu-id="dcf9b-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="dcf9b-110">Новый массив, содержащий элементы исходного массива вместе с их индексами.</span><span class="sxs-lookup"><span data-stu-id="dcf9b-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dcf9b-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="dcf9b-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="dcf9b-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="dcf9b-112">'TElement</span></span>

<span data-ttu-id="dcf9b-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="dcf9b-113">The type of elements of the array.</span></span>