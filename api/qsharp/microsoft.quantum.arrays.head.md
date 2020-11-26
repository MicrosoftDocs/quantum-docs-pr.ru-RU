---
uid: Microsoft.Quantum.Arrays.Head
title: Head, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 834cbe2384122463be6a0efcb6e09785aae9c092
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221119"
---
# <a name="head-function"></a><span data-ttu-id="55123-102">Head, функция</span><span class="sxs-lookup"><span data-stu-id="55123-102">Head function</span></span>

<span data-ttu-id="55123-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="55123-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="55123-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="55123-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="55123-105">Возвращает первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="55123-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="55123-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="55123-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="55123-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="55123-107">array : 'A[]</span></span>

<span data-ttu-id="55123-108">Массив, из которого берется первый элемент.</span><span class="sxs-lookup"><span data-stu-id="55123-108">Array of which the first element is taken.</span></span> <span data-ttu-id="55123-109">Длина массива должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="55123-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="55123-110">Выходные данные: ' A</span><span class="sxs-lookup"><span data-stu-id="55123-110">Output : 'A</span></span>

<span data-ttu-id="55123-111">Первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="55123-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="55123-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="55123-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="55123-113">' A</span><span class="sxs-lookup"><span data-stu-id="55123-113">'A</span></span>

<span data-ttu-id="55123-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="55123-114">The type of the array elements.</span></span>