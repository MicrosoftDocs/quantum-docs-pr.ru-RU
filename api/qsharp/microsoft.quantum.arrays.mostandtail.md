---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Функция Мостандтаил
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845591"
---
# <a name="mostandtail-function"></a><span data-ttu-id="fea3a-102">Функция Мостандтаил</span><span class="sxs-lookup"><span data-stu-id="fea3a-102">MostAndTail function</span></span>

<span data-ttu-id="fea3a-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fea3a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fea3a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fea3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fea3a-105">Возвращает кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="fea3a-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="fea3a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fea3a-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="fea3a-107">массив: ' A []</span><span class="sxs-lookup"><span data-stu-id="fea3a-107">array : 'A[]</span></span>

<span data-ttu-id="fea3a-108">Массив, содержащий по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="fea3a-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="fea3a-109">Выходные данные: ("A []," A)</span><span class="sxs-lookup"><span data-stu-id="fea3a-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="fea3a-110">Кортеж всех, кроме одного и последнего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="fea3a-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fea3a-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fea3a-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="fea3a-112">' A</span><span class="sxs-lookup"><span data-stu-id="fea3a-112">'A</span></span>

<span data-ttu-id="fea3a-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="fea3a-113">The type of the array elements.</span></span>