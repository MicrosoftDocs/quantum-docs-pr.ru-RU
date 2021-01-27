---
uid: Microsoft.Quantum.Arrays.Head
title: Head, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 6dd181914b5ed3ef16a02b31cb6131daf2a34e19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848576"
---
# <a name="head-function"></a><span data-ttu-id="ebf36-102">Head, функция</span><span class="sxs-lookup"><span data-stu-id="ebf36-102">Head function</span></span>

<span data-ttu-id="ebf36-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ebf36-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ebf36-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ebf36-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ebf36-105">Возвращает первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="ebf36-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="ebf36-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ebf36-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="ebf36-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="ebf36-107">array : 'A[]</span></span>

<span data-ttu-id="ebf36-108">Массив, из которого берется первый элемент.</span><span class="sxs-lookup"><span data-stu-id="ebf36-108">Array of which the first element is taken.</span></span> <span data-ttu-id="ebf36-109">Длина массива должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="ebf36-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="ebf36-110">Выходные данные: ' A</span><span class="sxs-lookup"><span data-stu-id="ebf36-110">Output : 'A</span></span>

<span data-ttu-id="ebf36-111">Первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="ebf36-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ebf36-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ebf36-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="ebf36-113">' A</span><span class="sxs-lookup"><span data-stu-id="ebf36-113">'A</span></span>

<span data-ttu-id="ebf36-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="ebf36-114">The type of the array elements.</span></span>