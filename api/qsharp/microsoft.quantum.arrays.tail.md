---
uid: Microsoft.Quantum.Arrays.Tail
title: Tail, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 7084cd8bc75f295024dce361153b58490074cdc5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220099"
---
# <a name="tail-function"></a><span data-ttu-id="8e439-102">Tail, функция</span><span class="sxs-lookup"><span data-stu-id="8e439-102">Tail function</span></span>

<span data-ttu-id="8e439-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8e439-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8e439-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e439-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e439-105">Возвращает последний элемент массива.</span><span class="sxs-lookup"><span data-stu-id="8e439-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="8e439-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8e439-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="8e439-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="8e439-107">array : 'A[]</span></span>

<span data-ttu-id="8e439-108">Массив, в котором взят последний элемент.</span><span class="sxs-lookup"><span data-stu-id="8e439-108">Array of which the last element is taken.</span></span> <span data-ttu-id="8e439-109">Длина массива должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="8e439-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="8e439-110">Выходные данные: ' A</span><span class="sxs-lookup"><span data-stu-id="8e439-110">Output : 'A</span></span>

<span data-ttu-id="8e439-111">Последний элемент массива.</span><span class="sxs-lookup"><span data-stu-id="8e439-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8e439-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8e439-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="8e439-113">' A</span><span class="sxs-lookup"><span data-stu-id="8e439-113">'A</span></span>

<span data-ttu-id="8e439-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="8e439-114">The type of the array elements.</span></span>