---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Функция префиксов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730064"
---
# <a name="prefixes-function"></a><span data-ttu-id="ec8f7-102">Функция префиксов</span><span class="sxs-lookup"><span data-stu-id="ec8f7-102">Prefixes function</span></span>

<span data-ttu-id="ec8f7-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ec8f7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ec8f7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec8f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec8f7-105">При наличии массива возвращает все его префиксы.</span><span class="sxs-lookup"><span data-stu-id="ec8f7-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="ec8f7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ec8f7-106">Description</span></span>

<span data-ttu-id="ec8f7-107">Возвращает массив всех префиксов, начиная с массива, у которого есть только первый элемент, вплоть до полного массива.</span><span class="sxs-lookup"><span data-stu-id="ec8f7-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="ec8f7-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ec8f7-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ec8f7-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="ec8f7-109">array : 'T[]</span></span>

<span data-ttu-id="ec8f7-110">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="ec8f7-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="ec8f7-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="ec8f7-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ec8f7-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ec8f7-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec8f7-113">Е</span><span class="sxs-lookup"><span data-stu-id="ec8f7-113">'T</span></span>

<span data-ttu-id="ec8f7-114">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="ec8f7-114">The type of `array` elements.</span></span>