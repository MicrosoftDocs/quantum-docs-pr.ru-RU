---
uid: Microsoft.Quantum.Arrays.Padded
title: Заполненная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730089"
---
# <a name="padded-function"></a><span data-ttu-id="ed9db-102">Заполненная функция</span><span class="sxs-lookup"><span data-stu-id="ed9db-102">Padded function</span></span>

<span data-ttu-id="ed9db-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ed9db-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ed9db-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed9db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed9db-105">Возвращает массив, дополненный с указанными значениями вплоть до указанной длины.</span><span class="sxs-lookup"><span data-stu-id="ed9db-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ed9db-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed9db-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="ed9db-107">Нелементстотал: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed9db-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed9db-108">Длина заполненного массива.</span><span class="sxs-lookup"><span data-stu-id="ed9db-108">The length of the padded array.</span></span> <span data-ttu-id="ed9db-109">Если это положительное значение, `inputArray` то оно дополняется заголовком.</span><span class="sxs-lookup"><span data-stu-id="ed9db-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="ed9db-110">Если это отрицательное значение, `inputArray` то оно дополняется на хвосте.</span><span class="sxs-lookup"><span data-stu-id="ed9db-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="ed9db-111">defaultElement: 'T</span><span class="sxs-lookup"><span data-stu-id="ed9db-111">defaultElement : 'T</span></span>

<span data-ttu-id="ed9db-112">Значение по умолчанию, используемое для заполнения элементов.</span><span class="sxs-lookup"><span data-stu-id="ed9db-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="ed9db-113">Инпутаррай: не[]</span><span class="sxs-lookup"><span data-stu-id="ed9db-113">inputArray : 'T[]</span></span>

<span data-ttu-id="ed9db-114">Массив, значения которого находятся в заголовке выходного массива.</span><span class="sxs-lookup"><span data-stu-id="ed9db-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="ed9db-115">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="ed9db-115">Output : 'T[]</span></span>

<span data-ttu-id="ed9db-116">Массив `output` , являющийся `inputArray` дополнением к заголовку с `defaultElement` s до `output` длины `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="ed9db-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ed9db-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ed9db-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed9db-118">Е</span><span class="sxs-lookup"><span data-stu-id="ed9db-118">'T</span></span>

<span data-ttu-id="ed9db-119">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="ed9db-119">The type of the array elements.</span></span>