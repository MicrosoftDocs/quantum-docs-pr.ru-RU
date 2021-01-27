---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: Операция Аппливисинпуттрансформатиона
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3ab07f301f310e3ec380981bdb53201fc74bd289
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841125"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="5215c-102">Операция Аппливисинпуттрансформатиона</span><span class="sxs-lookup"><span data-stu-id="5215c-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="5215c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5215c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5215c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5215c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5215c-105">При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="5215c-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="5215c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5215c-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="5215c-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="5215c-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="5215c-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="5215c-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="5215c-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="5215c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5215c-110">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="5215c-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="5215c-111">входные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="5215c-111">input : 'U</span></span>

<span data-ttu-id="5215c-112">Входные данные для функции.</span><span class="sxs-lookup"><span data-stu-id="5215c-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5215c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5215c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5215c-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5215c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5215c-115">Е</span><span class="sxs-lookup"><span data-stu-id="5215c-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="5215c-116">' U</span><span class="sxs-lookup"><span data-stu-id="5215c-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="5215c-117">Пример</span><span class="sxs-lookup"><span data-stu-id="5215c-117">Example</span></span>

<span data-ttu-id="5215c-118">Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для применения операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных входного типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="5215c-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="5215c-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="5215c-119">See Also</span></span>

- [<span data-ttu-id="5215c-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="5215c-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="5215c-121">Microsoft. тактов. Canon. Аппливисинпуттрансформатионк</span><span class="sxs-lookup"><span data-stu-id="5215c-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="5215c-122">Microsoft. тактов. Canon. Аппливисинпуттрансформатионка</span><span class="sxs-lookup"><span data-stu-id="5215c-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="5215c-123">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="5215c-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)