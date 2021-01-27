---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845510"
---
# <a name="prefixes-function"></a><span data-ttu-id="ae4f6-102">Функция префиксов</span><span class="sxs-lookup"><span data-stu-id="ae4f6-102">Prefixes function</span></span>

<span data-ttu-id="ae4f6-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ae4f6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ae4f6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae4f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae4f6-105">При наличии массива возвращает все его префиксы.</span><span class="sxs-lookup"><span data-stu-id="ae4f6-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="ae4f6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ae4f6-106">Description</span></span>

<span data-ttu-id="ae4f6-107">Возвращает массив всех префиксов, начиная с массива, у которого есть только первый элемент, вплоть до полного массива.</span><span class="sxs-lookup"><span data-stu-id="ae4f6-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="ae4f6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ae4f6-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ae4f6-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="ae4f6-109">array : 'T[]</span></span>

<span data-ttu-id="ae4f6-110">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="ae4f6-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="ae4f6-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="ae4f6-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ae4f6-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ae4f6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae4f6-113">Е</span><span class="sxs-lookup"><span data-stu-id="ae4f6-113">'T</span></span>

<span data-ttu-id="ae4f6-114">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="ae4f6-114">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="ae4f6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="ae4f6-115">Example</span></span>

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```