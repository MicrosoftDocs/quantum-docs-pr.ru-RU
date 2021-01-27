---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Функция Константаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846222"
---
# <a name="constantarray-function"></a><span data-ttu-id="e5be3-102">Функция Константаррай</span><span class="sxs-lookup"><span data-stu-id="e5be3-102">ConstantArray function</span></span>

<span data-ttu-id="e5be3-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e5be3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e5be3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e5be3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e5be3-105">Создает массив заданной длины со всеми элементами, равными заданному значению.</span><span class="sxs-lookup"><span data-stu-id="e5be3-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e5be3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5be3-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="e5be3-107">Длина: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e5be3-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e5be3-108">Длина нового массива.</span><span class="sxs-lookup"><span data-stu-id="e5be3-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="e5be3-109">значение: 'T</span><span class="sxs-lookup"><span data-stu-id="e5be3-109">value : 'T</span></span>

<span data-ttu-id="e5be3-110">Значение каждого элемента нового массива.</span><span class="sxs-lookup"><span data-stu-id="e5be3-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="e5be3-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="e5be3-111">Output : 'T[]</span></span>

<span data-ttu-id="e5be3-112">Новый массив длины `length` , каждый элемент которого имеет значение `value` .</span><span class="sxs-lookup"><span data-stu-id="e5be3-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e5be3-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e5be3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5be3-114">Е</span><span class="sxs-lookup"><span data-stu-id="e5be3-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="e5be3-115">Пример</span><span class="sxs-lookup"><span data-stu-id="e5be3-115">Example</span></span>

<span data-ttu-id="e5be3-116">Следующий код создает массив из трех логических значений, каждый из которых равен `true` :</span><span class="sxs-lookup"><span data-stu-id="e5be3-116">The following code creates an array of 3 Boolean values, each equal to `true`:</span></span>

```qsharp
let array = ConstantArray(3, true);
```