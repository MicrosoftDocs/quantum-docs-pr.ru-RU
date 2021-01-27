---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Функция Трансформедоператионка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840124"
---
# <a name="transformedoperationca-function"></a><span data-ttu-id="7a80c-102">Функция Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="7a80c-102">TransformedOperationCA function</span></span>

<span data-ttu-id="7a80c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7a80c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7a80c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7a80c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7a80c-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="7a80c-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7a80c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7a80c-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="7a80c-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="7a80c-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="7a80c-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="7a80c-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="7a80c-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="7a80c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7a80c-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a80c-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj--ctl"></a><span data-ttu-id="7a80c-111">Выходные данные: "U => [единица](xref:microsoft.quantum.lang-ref.unit)  —" года + CTL "</span><span class="sxs-lookup"><span data-stu-id="7a80c-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7a80c-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="7a80c-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7a80c-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7a80c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7a80c-114">Е</span><span class="sxs-lookup"><span data-stu-id="7a80c-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="7a80c-115">' U</span><span class="sxs-lookup"><span data-stu-id="7a80c-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="7a80c-116">Пример</span><span class="sxs-lookup"><span data-stu-id="7a80c-116">Example</span></span>

<span data-ttu-id="7a80c-117">Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для преобразования операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных, в операцию, которая принимает входные данные типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="7a80c-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="7a80c-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="7a80c-118">See Also</span></span>

- [<span data-ttu-id="7a80c-119">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="7a80c-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="7a80c-120">Microsoft. тактов. Canon. Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="7a80c-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="7a80c-121">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="7a80c-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="7a80c-122">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="7a80c-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="7a80c-123">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="7a80c-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)