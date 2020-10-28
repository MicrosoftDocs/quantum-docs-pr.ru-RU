---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: Функция Трансформедоператиона
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 349424a102dba7354bbaa65fffdc2b5d506a3b91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715328"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="15321-102">Функция Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="15321-102">TransformedOperationA function</span></span>

<span data-ttu-id="15321-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="15321-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="15321-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="15321-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="15321-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="15321-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="15321-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="15321-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="15321-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="15321-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="15321-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="15321-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="15321-109">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15321-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="15321-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="15321-110">The operation to be transformed.</span></span>



## <a name="output--u--unit-adj"></a><span data-ttu-id="15321-111">Выходные данные: "U = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="15321-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="15321-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="15321-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="15321-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="15321-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="15321-114">Е</span><span class="sxs-lookup"><span data-stu-id="15321-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="15321-115">' U</span><span class="sxs-lookup"><span data-stu-id="15321-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="15321-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="15321-116">See Also</span></span>

- [<span data-ttu-id="15321-117">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="15321-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="15321-118">Microsoft. тактов. Canon. Трансформедоператионк</span><span class="sxs-lookup"><span data-stu-id="15321-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="15321-119">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="15321-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="15321-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="15321-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="15321-121">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="15321-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)