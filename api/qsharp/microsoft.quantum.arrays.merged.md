---
uid: Microsoft.Quantum.Arrays.Merged
title: Объединенная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845612"
---
# <a name="merged-function"></a><span data-ttu-id="37c43-102">Объединенная функция</span><span class="sxs-lookup"><span data-stu-id="37c43-102">Merged function</span></span>

<span data-ttu-id="37c43-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="37c43-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="37c43-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37c43-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37c43-105">При наличии двух отсортированных массивов возвращает один массив, содержащий элементы обоих элементов в отсортированном порядке.</span><span class="sxs-lookup"><span data-stu-id="37c43-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="37c43-106">Используется для внутренних целей при сортировке слиянием.</span><span class="sxs-lookup"><span data-stu-id="37c43-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="37c43-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="37c43-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="37c43-108">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="37c43-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="37c43-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="37c43-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="37c43-110">Right: ' ' []</span><span class="sxs-lookup"><span data-stu-id="37c43-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="37c43-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="37c43-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37c43-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="37c43-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37c43-113">Е</span><span class="sxs-lookup"><span data-stu-id="37c43-113">'T</span></span>

