---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Функция Мостандтаил
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 8786250cf2f78ce2e9ff8baddc856d0bc07cb9a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730097"
---
# <a name="mostandtail-function"></a><span data-ttu-id="12838-102">Функция Мостандтаил</span><span class="sxs-lookup"><span data-stu-id="12838-102">MostAndTail function</span></span>

<span data-ttu-id="12838-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="12838-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="12838-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12838-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12838-105">Возвращает кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="12838-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="12838-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12838-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="12838-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="12838-107">array : 'A[]</span></span>

<span data-ttu-id="12838-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="12838-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="12838-109">Выходные данные: ("A []," A)</span><span class="sxs-lookup"><span data-stu-id="12838-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="12838-110">Кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="12838-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="12838-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="12838-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="12838-112">' A</span><span class="sxs-lookup"><span data-stu-id="12838-112">'A</span></span>

<span data-ttu-id="12838-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="12838-113">The type of the array elements.</span></span>