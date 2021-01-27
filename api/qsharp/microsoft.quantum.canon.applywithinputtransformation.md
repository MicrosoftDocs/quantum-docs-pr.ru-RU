---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Операция Аппливисинпуттрансформатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: d4589acbe9f9dc6c6ab665582ed663dbc193edbb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850375"
---
# <a name="applywithinputtransformation-operation"></a><span data-ttu-id="be5f0-102">Операция Аппливисинпуттрансформатион</span><span class="sxs-lookup"><span data-stu-id="be5f0-102">ApplyWithInputTransformation operation</span></span>

<span data-ttu-id="be5f0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be5f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be5f0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be5f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be5f0-105">При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="be5f0-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="be5f0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="be5f0-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="be5f0-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="be5f0-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="be5f0-108">Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.</span><span class="sxs-lookup"><span data-stu-id="be5f0-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="be5f0-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="be5f0-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="be5f0-110">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="be5f0-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="be5f0-111">входные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="be5f0-111">input : 'U</span></span>

<span data-ttu-id="be5f0-112">Входные данные для функции.</span><span class="sxs-lookup"><span data-stu-id="be5f0-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be5f0-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be5f0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="be5f0-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="be5f0-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="be5f0-115">Е</span><span class="sxs-lookup"><span data-stu-id="be5f0-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="be5f0-116">' U</span><span class="sxs-lookup"><span data-stu-id="be5f0-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="be5f0-117">Пример</span><span class="sxs-lookup"><span data-stu-id="be5f0-117">Example</span></span>

<span data-ttu-id="be5f0-118">Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для применения операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных входного типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="be5f0-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="be5f0-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="be5f0-119">See Also</span></span>

- [<span data-ttu-id="be5f0-120">Microsoft. тактов. Canon. Аппливисинпуттрансформатиона</span><span class="sxs-lookup"><span data-stu-id="be5f0-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="be5f0-121">Microsoft. тактов. Canon. Аппливисинпуттрансформатионк</span><span class="sxs-lookup"><span data-stu-id="be5f0-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="be5f0-122">Microsoft. тактов. Canon. Аппливисинпуттрансформатионка</span><span class="sxs-lookup"><span data-stu-id="be5f0-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="be5f0-123">Microsoft. тактов. Canon. Трансформедоператион</span><span class="sxs-lookup"><span data-stu-id="be5f0-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)