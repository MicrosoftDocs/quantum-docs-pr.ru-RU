---
uid: Microsoft.Quantum.Arrays.Flattened
title: Плоская функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848616"
---
# <a name="flattened-function"></a><span data-ttu-id="4bdeb-102">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="4bdeb-102">Flattened function</span></span>

<span data-ttu-id="4bdeb-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4bdeb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4bdeb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4bdeb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4bdeb-105">При наличии массива массивов возвращает объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="4bdeb-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="4bdeb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4bdeb-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="4bdeb-107">массивы: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="4bdeb-107">arrays : 'T[][]</span></span>

<span data-ttu-id="4bdeb-108">Массив массивов.</span><span class="sxs-lookup"><span data-stu-id="4bdeb-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="4bdeb-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="4bdeb-109">Output : 'T[]</span></span>

<span data-ttu-id="4bdeb-110">Объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="4bdeb-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4bdeb-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4bdeb-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4bdeb-112">Е</span><span class="sxs-lookup"><span data-stu-id="4bdeb-112">'T</span></span>

<span data-ttu-id="4bdeb-113">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="4bdeb-113">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="4bdeb-114">Пример</span><span class="sxs-lookup"><span data-stu-id="4bdeb-114">Example</span></span>

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```