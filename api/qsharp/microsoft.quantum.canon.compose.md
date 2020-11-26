---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216767"
---
# <a name="compose-function"></a><span data-ttu-id="fccce-102">Функция создания</span><span class="sxs-lookup"><span data-stu-id="fccce-102">Compose function</span></span>

<span data-ttu-id="fccce-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fccce-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fccce-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fccce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fccce-105">Возвращает композицию двух функций.</span><span class="sxs-lookup"><span data-stu-id="fccce-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="fccce-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fccce-106">Description</span></span>

<span data-ttu-id="fccce-107">При наличии двух функций $f $ и $g $ возвращает новую функцию, представляющую $f \Цирк g $.</span><span class="sxs-lookup"><span data-stu-id="fccce-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="fccce-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fccce-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="fccce-109">Внешний: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="fccce-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="fccce-110">Вторая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fccce-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="fccce-111">внутренний: не> "U</span><span class="sxs-lookup"><span data-stu-id="fccce-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="fccce-112">Первая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fccce-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="fccce-113">Выходные данные: 'T-> ' V</span><span class="sxs-lookup"><span data-stu-id="fccce-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="fccce-114">Новая функция $h $ таким, что для всех входных данных $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="fccce-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fccce-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fccce-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fccce-116">Е</span><span class="sxs-lookup"><span data-stu-id="fccce-116">'T</span></span>

<span data-ttu-id="fccce-117">Тип входных данных первой функции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="fccce-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="fccce-118">' U</span><span class="sxs-lookup"><span data-stu-id="fccce-118">'U</span></span>

<span data-ttu-id="fccce-119">Тип выходных данных первой функции, которая будет применена, и тип входных данных второй функции.</span><span class="sxs-lookup"><span data-stu-id="fccce-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="fccce-120">"V</span><span class="sxs-lookup"><span data-stu-id="fccce-120">'V</span></span>

<span data-ttu-id="fccce-121">Тип выходных данных второй функции, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fccce-121">The output type of the second function to be applied.</span></span>