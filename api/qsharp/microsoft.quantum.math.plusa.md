---
uid: Microsoft.Quantum.Math.PlusA
title: Функция и
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 14e9bfdbe4b70b4730e5bfc64a0ee81ab3cecaaf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842701"
---
# <a name="plusa-function"></a><span data-ttu-id="ac120-102">Функция и</span><span class="sxs-lookup"><span data-stu-id="ac120-102">PlusA function</span></span>

<span data-ttu-id="ac120-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ac120-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ac120-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac120-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac120-105">Возвращает сумму (объединение) двух входных значений.</span><span class="sxs-lookup"><span data-stu-id="ac120-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="ac120-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ac120-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="ac120-107">a: "Element []</span><span class="sxs-lookup"><span data-stu-id="ac120-107">a : 'Element[]</span></span>

<span data-ttu-id="ac120-108">Первый входной $a $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="ac120-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="ac120-109">b: ' element []</span><span class="sxs-lookup"><span data-stu-id="ac120-109">b : 'Element[]</span></span>

<span data-ttu-id="ac120-110">Второй входной $b $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="ac120-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="ac120-111">Выходные данные: ' element []</span><span class="sxs-lookup"><span data-stu-id="ac120-111">Output : 'Element[]</span></span>

<span data-ttu-id="ac120-112">Сумма $a + b $.</span><span class="sxs-lookup"><span data-stu-id="ac120-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ac120-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ac120-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="ac120-114">' Элемент</span><span class="sxs-lookup"><span data-stu-id="ac120-114">'Element</span></span>

<span data-ttu-id="ac120-115">Тип каждого элемента в каждом из двух входных массивов.</span><span class="sxs-lookup"><span data-stu-id="ac120-115">The type of each element in each of the two input arrays.</span></span>