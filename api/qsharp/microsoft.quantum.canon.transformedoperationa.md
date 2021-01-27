---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: Функция Трансформедоператиона
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: fac0fb6e03dc515892783fb4a5fa9cfc274550b8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840143"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="a92a8-102">Функция Трансформедоператиона</span><span class="sxs-lookup"><span data-stu-id="a92a8-102">TransformedOperationA function</span></span>

<span data-ttu-id="a92a8-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a92a8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a92a8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a92a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a92a8-105">При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.</span><span class="sxs-lookup"><span data-stu-id="a92a8-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="a92a8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a92a8-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="a92a8-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="a92a8-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="a92a8-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="a92a8-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="a92a8-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="a92a8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a92a8-110">Операция для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a92a8-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj"></a><span data-ttu-id="a92a8-111">Выходные данные: "U =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="a92a8-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a92a8-112">Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .</span><span class="sxs-lookup"><span data-stu-id="a92a8-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a92a8-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a92a8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a92a8-114">Е</span><span class="sxs-lookup"><span data-stu-id="a92a8-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="a92a8-115">' U</span><span class="sxs-lookup"><span data-stu-id="a92a8-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="a92a8-116">Пример</span><span class="sxs-lookup"><span data-stu-id="a92a8-116">Example</span></span>

<span data-ttu-id="a92a8-117">Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для преобразования операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных, в операцию, которая принимает входные данные типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="a92a8-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="a92a8-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="a92a8-118">See Also</span></span>

- [<span data-ttu-id="a92a8-119">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="a92a8-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="a92a8-120">Microsoft. тактов. Canon. Трансформедоператионк</span><span class="sxs-lookup"><span data-stu-id="a92a8-120">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="a92a8-121">Microsoft. тактов. Canon. Трансформедоператионка</span><span class="sxs-lookup"><span data-stu-id="a92a8-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="a92a8-122">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="a92a8-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="a92a8-123">Microsoft. тактов. Canon. составной</span><span class="sxs-lookup"><span data-stu-id="a92a8-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)