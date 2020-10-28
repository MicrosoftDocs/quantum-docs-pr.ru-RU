---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Несжатая функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729961"
---
# <a name="unzipped-function"></a><span data-ttu-id="a28ce-102">Несжатая функция</span><span class="sxs-lookup"><span data-stu-id="a28ce-102">Unzipped function</span></span>

<span data-ttu-id="a28ce-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a28ce-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a28ce-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a28ce-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a28ce-105">При наличии массива из двух кортежей функция возвращает кортеж с двумя массивами, каждый из которых содержит элементы кортежей входного массива.</span><span class="sxs-lookup"><span data-stu-id="a28ce-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="a28ce-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a28ce-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="a28ce-107">ARR: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="a28ce-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="a28ce-108">Массив, содержащий два кортежа</span><span class="sxs-lookup"><span data-stu-id="a28ce-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="a28ce-109">Выходные данные: ('T [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="a28ce-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="a28ce-110">Два массива, первый из которых содержит все первые элементы входных кортежей, второй из которых содержит все остальные элементы входных кортежей.</span><span class="sxs-lookup"><span data-stu-id="a28ce-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a28ce-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a28ce-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a28ce-112">Е</span><span class="sxs-lookup"><span data-stu-id="a28ce-112">'T</span></span>

<span data-ttu-id="a28ce-113">Тип первого элемента в каждом кортеже</span><span class="sxs-lookup"><span data-stu-id="a28ce-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="a28ce-114">' U</span><span class="sxs-lookup"><span data-stu-id="a28ce-114">'U</span></span>

<span data-ttu-id="a28ce-115">Тип второго элемента в каждом кортеже</span><span class="sxs-lookup"><span data-stu-id="a28ce-115">The type of the second element in each tuple</span></span>

## <a name="see-also"></a><span data-ttu-id="a28ce-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="a28ce-116">See Also</span></span>

- [<span data-ttu-id="a28ce-117">Microsoft.Quantum.Arrays.Zipпед</span><span class="sxs-lookup"><span data-stu-id="a28ce-117">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)