---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Функция Лукупфунктион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: db20795719d11138cbdc5a38c0a19d0f247af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220779"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="04deb-102">Функция Лукупфунктион</span><span class="sxs-lookup"><span data-stu-id="04deb-102">LookupFunction function</span></span>

<span data-ttu-id="04deb-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="04deb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="04deb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04deb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="04deb-105">При наличии массива возвращает функцию, которая возвращает элементы этого массива.</span><span class="sxs-lookup"><span data-stu-id="04deb-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="04deb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="04deb-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="04deb-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="04deb-107">array : 'T[]</span></span>

<span data-ttu-id="04deb-108">Массив, который будет представлен как функция уточняющего запроса.</span><span class="sxs-lookup"><span data-stu-id="04deb-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="04deb-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int) -></span><span class="sxs-lookup"><span data-stu-id="04deb-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="04deb-110">Функция `f` , которая `f(idx) == f[idx]` .</span><span class="sxs-lookup"><span data-stu-id="04deb-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="04deb-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="04deb-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="04deb-112">Е</span><span class="sxs-lookup"><span data-stu-id="04deb-112">'T</span></span>

<span data-ttu-id="04deb-113">Тип элементов массива, представленного в виде функции уточняющего запроса.</span><span class="sxs-lookup"><span data-stu-id="04deb-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="04deb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04deb-114">Remarks</span></span>

<span data-ttu-id="04deb-115">Эта функция в основном полезна для взаимодействия с функциями и операциями, которые принимают `Int -> 'T` в качестве аргументов функции.</span><span class="sxs-lookup"><span data-stu-id="04deb-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="04deb-116">Это обычно, например, в библиотеке представления генератора, где функции используются, чтобы избежать необходимости записи всего массива в памяти.</span><span class="sxs-lookup"><span data-stu-id="04deb-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>