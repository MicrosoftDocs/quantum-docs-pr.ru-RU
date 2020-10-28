---
uid: Microsoft.Quantum.Arrays.Head
title: Head, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 7b26a9c414ab2caad70f96f3c26c2d1cf0b03e95
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730225"
---
# <a name="head-function"></a><span data-ttu-id="66d0d-102">Head, функция</span><span class="sxs-lookup"><span data-stu-id="66d0d-102">Head function</span></span>

<span data-ttu-id="66d0d-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="66d0d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="66d0d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="66d0d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="66d0d-105">Возвращает первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="66d0d-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="66d0d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66d0d-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="66d0d-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="66d0d-107">array : 'A[]</span></span>

<span data-ttu-id="66d0d-108">Массив, из которого берется первый элемент.</span><span class="sxs-lookup"><span data-stu-id="66d0d-108">Array of which the first element is taken.</span></span> <span data-ttu-id="66d0d-109">Длина массива должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="66d0d-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="66d0d-110">Выходные данные: ' A</span><span class="sxs-lookup"><span data-stu-id="66d0d-110">Output : 'A</span></span>

<span data-ttu-id="66d0d-111">Первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="66d0d-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66d0d-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="66d0d-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="66d0d-113">' A</span><span class="sxs-lookup"><span data-stu-id="66d0d-113">'A</span></span>

<span data-ttu-id="66d0d-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="66d0d-114">The type of the array elements.</span></span>