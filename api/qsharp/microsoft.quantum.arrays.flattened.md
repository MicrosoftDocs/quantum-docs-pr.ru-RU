---
uid: Microsoft.Quantum.Arrays.Flattened
title: Плоская функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 91a35f0ac2c2f8609bac07734265fcf4e88bf50b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730264"
---
# <a name="flattened-function"></a><span data-ttu-id="898ec-102">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="898ec-102">Flattened function</span></span>

<span data-ttu-id="898ec-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="898ec-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="898ec-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="898ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="898ec-105">При наличии массива массивов возвращает объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="898ec-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="898ec-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="898ec-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="898ec-107">массивы: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="898ec-107">arrays : 'T[][]</span></span>

<span data-ttu-id="898ec-108">Массив массивов.</span><span class="sxs-lookup"><span data-stu-id="898ec-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="898ec-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="898ec-109">Output : 'T[]</span></span>

<span data-ttu-id="898ec-110">Объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="898ec-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="898ec-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="898ec-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="898ec-112">Е</span><span class="sxs-lookup"><span data-stu-id="898ec-112">'T</span></span>

<span data-ttu-id="898ec-113">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="898ec-113">The type of `array` elements.</span></span>