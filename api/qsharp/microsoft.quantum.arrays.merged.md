---
uid: Microsoft.Quantum.Arrays.Merged
title: Объединенная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: b3383f8a04e6fa23562aa81e5b911d06752f4fb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220643"
---
# <a name="merged-function"></a><span data-ttu-id="85193-102">Объединенная функция</span><span class="sxs-lookup"><span data-stu-id="85193-102">Merged function</span></span>

<span data-ttu-id="85193-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="85193-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="85193-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85193-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85193-105">При наличии двух отсортированных массивов возвращает один массив, содержащий элементы обоих элементов в отсортированном порядке.</span><span class="sxs-lookup"><span data-stu-id="85193-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="85193-106">Используется для внутренних целей при сортировке слиянием.</span><span class="sxs-lookup"><span data-stu-id="85193-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="85193-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="85193-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="85193-108">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="85193-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="85193-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="85193-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="85193-110">Right: ' ' []</span><span class="sxs-lookup"><span data-stu-id="85193-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="85193-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="85193-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="85193-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="85193-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="85193-113">Е</span><span class="sxs-lookup"><span data-stu-id="85193-113">'T</span></span>

