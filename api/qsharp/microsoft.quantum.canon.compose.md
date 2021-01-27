---
uid: Microsoft.Quantum.Canon.Compose
title: Функция создания
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840907"
---
# <a name="compose-function"></a><span data-ttu-id="fd596-102">Функция создания</span><span class="sxs-lookup"><span data-stu-id="fd596-102">Compose function</span></span>

<span data-ttu-id="fd596-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fd596-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fd596-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd596-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd596-105">Возвращает композицию двух функций.</span><span class="sxs-lookup"><span data-stu-id="fd596-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="fd596-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fd596-106">Description</span></span>

<span data-ttu-id="fd596-107">При наличии двух функций $f $ и $g $ возвращает новую функцию, представляющую $f \Цирк g $.</span><span class="sxs-lookup"><span data-stu-id="fd596-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="fd596-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd596-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="fd596-109">Внешний: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="fd596-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="fd596-110">Вторая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fd596-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="fd596-111">внутренний: не> "U</span><span class="sxs-lookup"><span data-stu-id="fd596-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="fd596-112">Первая функция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fd596-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="fd596-113">Выходные данные: 'T-> ' V</span><span class="sxs-lookup"><span data-stu-id="fd596-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="fd596-114">Новая функция $h $ таким, что для всех входных данных $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="fd596-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fd596-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fd596-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fd596-116">Е</span><span class="sxs-lookup"><span data-stu-id="fd596-116">'T</span></span>

<span data-ttu-id="fd596-117">Тип входных данных первой функции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="fd596-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="fd596-118">' U</span><span class="sxs-lookup"><span data-stu-id="fd596-118">'U</span></span>

<span data-ttu-id="fd596-119">Тип выходных данных первой функции, которая будет применена, и тип входных данных второй функции.</span><span class="sxs-lookup"><span data-stu-id="fd596-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="fd596-120">"V</span><span class="sxs-lookup"><span data-stu-id="fd596-120">'V</span></span>

<span data-ttu-id="fd596-121">Тип выходных данных второй функции, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="fd596-121">The output type of the second function to be applied.</span></span>