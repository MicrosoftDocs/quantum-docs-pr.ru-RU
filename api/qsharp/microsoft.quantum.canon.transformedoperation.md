---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: Функция Трансформедоператион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: d8c2f52290ce89d0a8ff138ba25f6b2e5e0516d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715341"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="57b70-102">Функция Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="57b70-102">TransformedOperation function</span></span>

<span data-ttu-id="57b70-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="57b70-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="57b70-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="57b70-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="57b70-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="57b70-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="57b70-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="57b70-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="57b70-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="57b70-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="57b70-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="57b70-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="57b70-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="57b70-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="57b70-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="57b70-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="57b70-111">Выходные данные: "U =>ная [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="57b70-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="57b70-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="57b70-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="57b70-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="57b70-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="57b70-114">Е</span><span class="sxs-lookup"><span data-stu-id="57b70-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="57b70-115">' U</span><span class="sxs-lookup"><span data-stu-id="57b70-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="57b70-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="57b70-116">See Also</span></span>

- [<span data-ttu-id="57b70-117">Microsoft. тактов. Canon. Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="57b70-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="57b70-118">Microsoft. тактов. Canon. Трансформедоператионк</span><span class="sxs-lookup"><span data-stu-id="57b70-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="57b70-119">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="57b70-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="57b70-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="57b70-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="57b70-121">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="57b70-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)