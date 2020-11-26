---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: Функция Трансформедоператион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: a26cc178f67fd99324355ac230d9e91081b6e238
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204935"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="455af-102">Функция Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="455af-102">TransformedOperation function</span></span>

<span data-ttu-id="455af-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="455af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="455af-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="455af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="455af-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="455af-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="455af-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="455af-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="455af-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="455af-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="455af-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="455af-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="455af-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="455af-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="455af-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="455af-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="455af-111">Выходные данные: "U =>ная [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="455af-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="455af-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="455af-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="455af-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="455af-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="455af-114">Е</span><span class="sxs-lookup"><span data-stu-id="455af-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="455af-115">' U</span><span class="sxs-lookup"><span data-stu-id="455af-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="455af-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="455af-116">See Also</span></span>

- [<span data-ttu-id="455af-117">Microsoft. тактов. Canon. Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="455af-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="455af-118">Microsoft. тактов. Canon. Трансформедоператионк</span><span class="sxs-lookup"><span data-stu-id="455af-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="455af-119">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="455af-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="455af-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="455af-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="455af-121">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="455af-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)