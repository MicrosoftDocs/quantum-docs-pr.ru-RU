---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716490"
---
# <a name="compose-function"></a><span data-ttu-id="0dc4a-102">Функция создания</span><span class="sxs-lookup"><span data-stu-id="0dc4a-102">Compose function</span></span>

<span data-ttu-id="0dc4a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0dc4a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0dc4a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0dc4a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0dc4a-105">Возвращает композицию двух функций.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="0dc4a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0dc4a-106">Description</span></span>

<span data-ttu-id="0dc4a-107">При наличии двух функций $f $ и $g $ возвращает новую функцию, представляющую $f \Цирк g $.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="0dc4a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0dc4a-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="0dc4a-109">Внешний: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="0dc4a-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="0dc4a-110">Вторая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="0dc4a-111">внутренний: не> "U</span><span class="sxs-lookup"><span data-stu-id="0dc4a-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="0dc4a-112">Первая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="0dc4a-113">Выходные данные: 'T-> ' V</span><span class="sxs-lookup"><span data-stu-id="0dc4a-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="0dc4a-114">Новая функция $h $ таким, что для всех входных данных $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0dc4a-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0dc4a-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0dc4a-116">Е</span><span class="sxs-lookup"><span data-stu-id="0dc4a-116">'T</span></span>

<span data-ttu-id="0dc4a-117">Тип входных данных первой функции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="0dc4a-118">' U</span><span class="sxs-lookup"><span data-stu-id="0dc4a-118">'U</span></span>

<span data-ttu-id="0dc4a-119">Тип выходных данных первой функции, которая будет применена, и тип входных данных второй функции.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="0dc4a-120">"V</span><span class="sxs-lookup"><span data-stu-id="0dc4a-120">'V</span></span>

<span data-ttu-id="0dc4a-121">Тип выходных данных второй функции, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-121">The output type of the second function to be applied.</span></span>