---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Функция Трансформедоператионка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: fa204433dc8195dd27fa40980fb2262f8a3848bb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204850"
---
# <a name="transformedoperationca-function"></a><span data-ttu-id="20639-102">Функция Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="20639-102">TransformedOperationCA function</span></span>

<span data-ttu-id="20639-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="20639-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="20639-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20639-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20639-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="20639-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="20639-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20639-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="20639-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="20639-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="20639-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="20639-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="20639-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="20639-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="20639-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="20639-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj--ctl"></a><span data-ttu-id="20639-111">Выходные данные: "U => [единица](xref:microsoft.quantum.lang-ref.unit)  —" года + CTL "</span><span class="sxs-lookup"><span data-stu-id="20639-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="20639-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="20639-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="20639-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="20639-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="20639-114">Е</span><span class="sxs-lookup"><span data-stu-id="20639-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="20639-115">' U</span><span class="sxs-lookup"><span data-stu-id="20639-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="20639-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="20639-116">See Also</span></span>

- [<span data-ttu-id="20639-117">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="20639-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="20639-118">Microsoft. тактов. Canon. Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="20639-118">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="20639-119">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="20639-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="20639-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="20639-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="20639-121">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="20639-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)