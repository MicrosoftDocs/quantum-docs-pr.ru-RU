---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Функция Мостандтаил
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220575"
---
# <a name="mostandtail-function"></a><span data-ttu-id="2d670-102">Функция Мостандтаил</span><span class="sxs-lookup"><span data-stu-id="2d670-102">MostAndTail function</span></span>

<span data-ttu-id="2d670-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2d670-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2d670-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2d670-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2d670-105">Возвращает кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="2d670-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="2d670-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2d670-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="2d670-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="2d670-107">array : 'A[]</span></span>

<span data-ttu-id="2d670-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="2d670-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="2d670-109">Выходные данные: ("A []," A)</span><span class="sxs-lookup"><span data-stu-id="2d670-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="2d670-110">Кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="2d670-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2d670-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2d670-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="2d670-112">' A</span><span class="sxs-lookup"><span data-stu-id="2d670-112">'A</span></span>

<span data-ttu-id="2d670-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="2d670-113">The type of the array elements.</span></span>