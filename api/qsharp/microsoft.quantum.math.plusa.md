---
uid: Microsoft.Quantum.Math.PlusA
title: Функция и
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: fe19c5d2e075624516376a5d5fa49014acb295ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194837"
---
# <a name="plusa-function"></a><span data-ttu-id="8405a-102">Функция и</span><span class="sxs-lookup"><span data-stu-id="8405a-102">PlusA function</span></span>

<span data-ttu-id="8405a-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8405a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8405a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8405a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8405a-105">Возвращает сумму (объединение) двух входных значений.</span><span class="sxs-lookup"><span data-stu-id="8405a-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="8405a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8405a-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="8405a-107">a: "Element []</span><span class="sxs-lookup"><span data-stu-id="8405a-107">a : 'Element[]</span></span>

<span data-ttu-id="8405a-108">Первый входной $a $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="8405a-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="8405a-109">b: ' element []</span><span class="sxs-lookup"><span data-stu-id="8405a-109">b : 'Element[]</span></span>

<span data-ttu-id="8405a-110">Второй входной $b $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="8405a-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="8405a-111">Выходные данные: ' element []</span><span class="sxs-lookup"><span data-stu-id="8405a-111">Output : 'Element[]</span></span>

<span data-ttu-id="8405a-112">Сумма $a + b $.</span><span class="sxs-lookup"><span data-stu-id="8405a-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8405a-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8405a-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="8405a-114">' Элемент</span><span class="sxs-lookup"><span data-stu-id="8405a-114">'Element</span></span>

<span data-ttu-id="8405a-115">Тип каждого элемента в каждом из двух входных массивов.</span><span class="sxs-lookup"><span data-stu-id="8405a-115">The type of each element in each of the two input arrays.</span></span>