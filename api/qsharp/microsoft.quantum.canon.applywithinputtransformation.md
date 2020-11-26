---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Операция Аппливисинпуттрансформатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3586e9a114a550fb1989186e9c18fe4f344cf060
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217192"
---
# <a name="applywithinputtransformation-operation"></a><span data-ttu-id="3055c-102">Операция Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="3055c-102">ApplyWithInputTransformation operation</span></span>

<span data-ttu-id="3055c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3055c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3055c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3055c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3055c-105">При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="3055c-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="3055c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3055c-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="3055c-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="3055c-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="3055c-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="3055c-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="3055c-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="3055c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="3055c-110">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="3055c-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="3055c-111">входные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="3055c-111">input : 'U</span></span>

<span data-ttu-id="3055c-112">Входные данные для функции.</span><span class="sxs-lookup"><span data-stu-id="3055c-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3055c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3055c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3055c-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3055c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3055c-115">Е</span><span class="sxs-lookup"><span data-stu-id="3055c-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="3055c-116">' U</span><span class="sxs-lookup"><span data-stu-id="3055c-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="3055c-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="3055c-117">See Also</span></span>

- [<span data-ttu-id="3055c-118">Microsoft. тактов. Canon. Аппливисинпуттрансформатиона</span><span class="sxs-lookup"><span data-stu-id="3055c-118">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="3055c-119">Microsoft. тактов. Canon. Аппливисинпуттрансформатионк</span><span class="sxs-lookup"><span data-stu-id="3055c-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="3055c-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатионка</span><span class="sxs-lookup"><span data-stu-id="3055c-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="3055c-121">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="3055c-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)