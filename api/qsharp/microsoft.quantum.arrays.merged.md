---
uid: Microsoft.Quantum.Arrays.Merged
title: Объединенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730112"
---
# <a name="merged-function"></a><span data-ttu-id="75fc3-102">Объединенная функция</span><span class="sxs-lookup"><span data-stu-id="75fc3-102">Merged function</span></span>

<span data-ttu-id="75fc3-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="75fc3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="75fc3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="75fc3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="75fc3-105">При наличии двух отсортированных массивов возвращает один массив, содержащий элементы обоих элементов в отсортированном порядке.</span><span class="sxs-lookup"><span data-stu-id="75fc3-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="75fc3-106">Используется для внутренних целей при сортировке слиянием.</span><span class="sxs-lookup"><span data-stu-id="75fc3-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="75fc3-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="75fc3-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="75fc3-108">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="75fc3-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="75fc3-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="75fc3-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="75fc3-110">Right: ' ' []</span><span class="sxs-lookup"><span data-stu-id="75fc3-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="75fc3-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="75fc3-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="75fc3-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="75fc3-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="75fc3-113">Е</span><span class="sxs-lookup"><span data-stu-id="75fc3-113">'T</span></span>

