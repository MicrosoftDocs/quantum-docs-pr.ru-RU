---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Операция Аппливисинпуттрансформатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 2b7863337ef724d9c3ba10201a9a01d0b2226ea8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716867"
---
# <a name="applywithinputtransformation-operation"></a><span data-ttu-id="8c9c8-102">Операция Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="8c9c8-102">ApplyWithInputTransformation operation</span></span>

<span data-ttu-id="8c9c8-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8c9c8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8c9c8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c9c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8c9c8-105">При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="8c9c8-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="8c9c8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8c9c8-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="8c9c8-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="8c9c8-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="8c9c8-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="8c9c8-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="8c9c8-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="8c9c8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8c9c8-110">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="8c9c8-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="8c9c8-111">входные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="8c9c8-111">input : 'U</span></span>

<span data-ttu-id="8c9c8-112">Входные данные для функции.</span><span class="sxs-lookup"><span data-stu-id="8c9c8-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8c9c8-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c9c8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8c9c8-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8c9c8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8c9c8-115">Е</span><span class="sxs-lookup"><span data-stu-id="8c9c8-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="8c9c8-116">' U</span><span class="sxs-lookup"><span data-stu-id="8c9c8-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="8c9c8-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="8c9c8-117">See Also</span></span>

- [<span data-ttu-id="8c9c8-118">Microsoft. тактов. Canon. Аппливисинпуттрансформатиона</span><span class="sxs-lookup"><span data-stu-id="8c9c8-118">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="8c9c8-119">Microsoft. тактов. Canon. Аппливисинпуттрансформатионк</span><span class="sxs-lookup"><span data-stu-id="8c9c8-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="8c9c8-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатионка</span><span class="sxs-lookup"><span data-stu-id="8c9c8-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="8c9c8-121">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="8c9c8-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)