---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Функция Константаррай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210069"
---
# <a name="constantarray-function"></a><span data-ttu-id="55701-102">Функция Константаррай</span><span class="sxs-lookup"><span data-stu-id="55701-102">ConstantArray function</span></span>

<span data-ttu-id="55701-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="55701-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="55701-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="55701-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="55701-105">Создает массив заданной длины со всеми элементами, равными заданному значению.</span><span class="sxs-lookup"><span data-stu-id="55701-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="55701-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="55701-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="55701-107">Длина: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="55701-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="55701-108">Длина нового массива.</span><span class="sxs-lookup"><span data-stu-id="55701-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="55701-109">значение: 'T</span><span class="sxs-lookup"><span data-stu-id="55701-109">value : 'T</span></span>

<span data-ttu-id="55701-110">Значение каждого элемента нового массива.</span><span class="sxs-lookup"><span data-stu-id="55701-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="55701-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="55701-111">Output : 'T[]</span></span>

<span data-ttu-id="55701-112">Новый массив длины `length` , каждый элемент которого имеет значение `value` .</span><span class="sxs-lookup"><span data-stu-id="55701-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="55701-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="55701-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="55701-114">Е</span><span class="sxs-lookup"><span data-stu-id="55701-114">'T</span></span>

