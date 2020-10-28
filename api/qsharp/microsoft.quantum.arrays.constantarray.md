---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Функция Константаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730377"
---
# <a name="constantarray-function"></a><span data-ttu-id="61e9c-102">Функция Константаррай</span><span class="sxs-lookup"><span data-stu-id="61e9c-102">ConstantArray function</span></span>

<span data-ttu-id="61e9c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="61e9c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="61e9c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="61e9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="61e9c-105">Создает массив заданной длины со всеми элементами, равными заданному значению.</span><span class="sxs-lookup"><span data-stu-id="61e9c-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="61e9c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="61e9c-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="61e9c-107">Длина: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="61e9c-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="61e9c-108">Длина нового массива.</span><span class="sxs-lookup"><span data-stu-id="61e9c-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="61e9c-109">значение: 'T</span><span class="sxs-lookup"><span data-stu-id="61e9c-109">value : 'T</span></span>

<span data-ttu-id="61e9c-110">Значение каждого элемента нового массива.</span><span class="sxs-lookup"><span data-stu-id="61e9c-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="61e9c-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="61e9c-111">Output : 'T[]</span></span>

<span data-ttu-id="61e9c-112">Новый массив длины `length` , каждый элемент которого имеет значение `value` .</span><span class="sxs-lookup"><span data-stu-id="61e9c-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="61e9c-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="61e9c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="61e9c-114">Е</span><span class="sxs-lookup"><span data-stu-id="61e9c-114">'T</span></span>

