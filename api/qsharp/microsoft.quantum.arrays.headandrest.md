---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221085"
---
# <a name="headandrest-function"></a><span data-ttu-id="1cd95-102">Функция Хеадандрест</span><span class="sxs-lookup"><span data-stu-id="1cd95-102">HeadAndRest function</span></span>

<span data-ttu-id="1cd95-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1cd95-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1cd95-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1cd95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1cd95-105">Возвращает кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="1cd95-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="1cd95-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1cd95-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="1cd95-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="1cd95-107">array : 'A[]</span></span>

<span data-ttu-id="1cd95-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="1cd95-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="1cd95-109">Выходные данные: (' а, ' A [])</span><span class="sxs-lookup"><span data-stu-id="1cd95-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="1cd95-110">Кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="1cd95-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1cd95-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="1cd95-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="1cd95-112">' A</span><span class="sxs-lookup"><span data-stu-id="1cd95-112">'A</span></span>

<span data-ttu-id="1cd95-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="1cd95-113">The type of the array elements.</span></span>