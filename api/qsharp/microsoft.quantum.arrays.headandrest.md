---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848548"
---
# <a name="headandrest-function"></a><span data-ttu-id="552d4-102">Функция Хеадандрест</span><span class="sxs-lookup"><span data-stu-id="552d4-102">HeadAndRest function</span></span>

<span data-ttu-id="552d4-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="552d4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="552d4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="552d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="552d4-105">Возвращает кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="552d4-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="552d4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="552d4-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="552d4-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="552d4-107">array : 'A[]</span></span>

<span data-ttu-id="552d4-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="552d4-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="552d4-109">Выходные данные: (' а, ' A [])</span><span class="sxs-lookup"><span data-stu-id="552d4-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="552d4-110">Кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="552d4-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="552d4-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="552d4-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="552d4-112">' A</span><span class="sxs-lookup"><span data-stu-id="552d4-112">'A</span></span>

<span data-ttu-id="552d4-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="552d4-113">The type of the array elements.</span></span>