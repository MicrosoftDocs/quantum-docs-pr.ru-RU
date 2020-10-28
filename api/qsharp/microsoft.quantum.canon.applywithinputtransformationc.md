---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: Операция Аппливисинпуттрансформатионк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: f166880d3ca8a7fc45635c0105aa5c83fe1b4f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716840"
---
# <a name="applywithinputtransformationc-operation"></a><span data-ttu-id="4834a-102">Операция Аппливисинпуттрансформатионк</span><span class="sxs-lookup"><span data-stu-id="4834a-102">ApplyWithInputTransformationC operation</span></span>

<span data-ttu-id="4834a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4834a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4834a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4834a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4834a-105">При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="4834a-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="4834a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4834a-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="4834a-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="4834a-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="4834a-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="4834a-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="4834a-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="4834a-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="4834a-110">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="4834a-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="4834a-111">входные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="4834a-111">input : 'U</span></span>

<span data-ttu-id="4834a-112">Входные данные для функции.</span><span class="sxs-lookup"><span data-stu-id="4834a-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4834a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4834a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4834a-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4834a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4834a-115">Е</span><span class="sxs-lookup"><span data-stu-id="4834a-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="4834a-116">' U</span><span class="sxs-lookup"><span data-stu-id="4834a-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="4834a-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="4834a-117">See Also</span></span>

- [<span data-ttu-id="4834a-118">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="4834a-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="4834a-119">Microsoft. тактов. Canon. Аппливисинпуттрансформатиона</span><span class="sxs-lookup"><span data-stu-id="4834a-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="4834a-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатионка</span><span class="sxs-lookup"><span data-stu-id="4834a-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="4834a-121">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="4834a-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)