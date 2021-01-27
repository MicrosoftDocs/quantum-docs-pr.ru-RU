---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Несжатая функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845378"
---
# <a name="unzipped-function"></a><span data-ttu-id="a7114-102">Несжатая функция</span><span class="sxs-lookup"><span data-stu-id="a7114-102">Unzipped function</span></span>

<span data-ttu-id="a7114-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a7114-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a7114-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7114-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7114-105">При наличии массива из двух кортежей функция возвращает кортеж с двумя массивами, каждый из которых содержит элементы кортежей входного массива.</span><span class="sxs-lookup"><span data-stu-id="a7114-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="a7114-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a7114-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="a7114-107">ARR: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="a7114-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="a7114-108">Массив, содержащий два кортежа</span><span class="sxs-lookup"><span data-stu-id="a7114-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="a7114-109">Выходные данные: ('T [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="a7114-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="a7114-110">Два массива, первый из которых содержит все первые элементы входных кортежей, второй из которых содержит все остальные элементы входных кортежей.</span><span class="sxs-lookup"><span data-stu-id="a7114-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a7114-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a7114-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a7114-112">Е</span><span class="sxs-lookup"><span data-stu-id="a7114-112">'T</span></span>

<span data-ttu-id="a7114-113">Тип первого элемента в каждом кортеже</span><span class="sxs-lookup"><span data-stu-id="a7114-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="a7114-114">' U</span><span class="sxs-lookup"><span data-stu-id="a7114-114">'U</span></span>

<span data-ttu-id="a7114-115">Тип второго элемента в каждом кортеже</span><span class="sxs-lookup"><span data-stu-id="a7114-115">The type of the second element in each tuple</span></span>

## <a name="example"></a><span data-ttu-id="a7114-116">Пример</span><span class="sxs-lookup"><span data-stu-id="a7114-116">Example</span></span>

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a><span data-ttu-id="a7114-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="a7114-117">See Also</span></span>

- [<span data-ttu-id="a7114-118">Microsoft.Quantum.Arrays.Zipпед</span><span class="sxs-lookup"><span data-stu-id="a7114-118">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)