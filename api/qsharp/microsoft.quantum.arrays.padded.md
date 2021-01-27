---
uid: Microsoft.Quantum.Arrays.Padded
title: Заполненная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845565"
---
# <a name="padded-function"></a><span data-ttu-id="8fa1c-102">Заполненная функция</span><span class="sxs-lookup"><span data-stu-id="8fa1c-102">Padded function</span></span>

<span data-ttu-id="8fa1c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8fa1c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8fa1c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fa1c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fa1c-105">Возвращает массив, дополненный с указанными значениями вплоть до указанной длины.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8fa1c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8fa1c-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="8fa1c-107">Нелементстотал: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8fa1c-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8fa1c-108">Длина заполненного массива.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-108">The length of the padded array.</span></span> <span data-ttu-id="8fa1c-109">Если это положительное значение, `inputArray` то оно дополняется заголовком.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="8fa1c-110">Если это отрицательное значение, `inputArray` то оно дополняется на хвосте.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="8fa1c-111">defaultElement: 'T</span><span class="sxs-lookup"><span data-stu-id="8fa1c-111">defaultElement : 'T</span></span>

<span data-ttu-id="8fa1c-112">Значение по умолчанию, используемое для заполнения элементов.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="8fa1c-113">Инпутаррай: не[]</span><span class="sxs-lookup"><span data-stu-id="8fa1c-113">inputArray : 'T[]</span></span>

<span data-ttu-id="8fa1c-114">Массив, значения которого находятся в заголовке выходного массива.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="8fa1c-115">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="8fa1c-115">Output : 'T[]</span></span>

<span data-ttu-id="8fa1c-116">Массив `output` , являющийся `inputArray` дополнением к заголовку с `defaultElement` s до `output` длины `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="8fa1c-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8fa1c-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8fa1c-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8fa1c-118">Е</span><span class="sxs-lookup"><span data-stu-id="8fa1c-118">'T</span></span>

<span data-ttu-id="8fa1c-119">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="8fa1c-119">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="8fa1c-120">Пример</span><span class="sxs-lookup"><span data-stu-id="8fa1c-120">Example</span></span>

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```