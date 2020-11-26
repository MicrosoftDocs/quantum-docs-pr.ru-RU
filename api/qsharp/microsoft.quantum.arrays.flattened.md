---
uid: Microsoft.Quantum.Arrays.Flattened
title: Плоская функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 331b1714109259b21982e99d030aa0662e3aaadb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221221"
---
# <a name="flattened-function"></a><span data-ttu-id="67645-102">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="67645-102">Flattened function</span></span>

<span data-ttu-id="67645-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="67645-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="67645-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67645-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="67645-105">При наличии массива массивов возвращает объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="67645-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="67645-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67645-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="67645-107">массивы: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="67645-107">arrays : 'T[][]</span></span>

<span data-ttu-id="67645-108">Массив массивов.</span><span class="sxs-lookup"><span data-stu-id="67645-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="67645-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="67645-109">Output : 'T[]</span></span>

<span data-ttu-id="67645-110">Объединение всех массивов.</span><span class="sxs-lookup"><span data-stu-id="67645-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="67645-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="67645-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67645-112">Е</span><span class="sxs-lookup"><span data-stu-id="67645-112">'T</span></span>

<span data-ttu-id="67645-113">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="67645-113">The type of `array` elements.</span></span>