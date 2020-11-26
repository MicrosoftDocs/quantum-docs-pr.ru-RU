---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220400"
---
# <a name="prefixes-function"></a><span data-ttu-id="71cf5-102">Функция префиксов</span><span class="sxs-lookup"><span data-stu-id="71cf5-102">Prefixes function</span></span>

<span data-ttu-id="71cf5-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="71cf5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="71cf5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71cf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71cf5-105">При наличии массива возвращает все его префиксы.</span><span class="sxs-lookup"><span data-stu-id="71cf5-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="71cf5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="71cf5-106">Description</span></span>

<span data-ttu-id="71cf5-107">Возвращает массив всех префиксов, начиная с массива, у которого есть только первый элемент, вплоть до полного массива.</span><span class="sxs-lookup"><span data-stu-id="71cf5-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="71cf5-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="71cf5-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="71cf5-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="71cf5-109">array : 'T[]</span></span>

<span data-ttu-id="71cf5-110">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="71cf5-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="71cf5-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="71cf5-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="71cf5-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="71cf5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71cf5-113">Е</span><span class="sxs-lookup"><span data-stu-id="71cf5-113">'T</span></span>

<span data-ttu-id="71cf5-114">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="71cf5-114">The type of `array` elements.</span></span>