---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730224"
---
# <a name="headandrest-function"></a><span data-ttu-id="38401-102">Функция Хеадандрест</span><span class="sxs-lookup"><span data-stu-id="38401-102">HeadAndRest function</span></span>

<span data-ttu-id="38401-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="38401-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="38401-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="38401-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="38401-105">Возвращает кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="38401-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="38401-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="38401-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="38401-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="38401-107">array : 'A[]</span></span>

<span data-ttu-id="38401-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="38401-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="38401-109">Выходные данные: (' а, ' A [])</span><span class="sxs-lookup"><span data-stu-id="38401-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="38401-110">Кортеж из первого и всех остальных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="38401-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="38401-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="38401-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="38401-112">' A</span><span class="sxs-lookup"><span data-stu-id="38401-112">'A</span></span>

<span data-ttu-id="38401-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="38401-113">The type of the array elements.</span></span>