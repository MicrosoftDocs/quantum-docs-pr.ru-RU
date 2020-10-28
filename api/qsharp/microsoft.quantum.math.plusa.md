---
uid: Microsoft.Quantum.Math.PlusA
title: Функция и
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709602"
---
# <a name="plusa-function"></a><span data-ttu-id="50b5f-102">Функция и</span><span class="sxs-lookup"><span data-stu-id="50b5f-102">PlusA function</span></span>

<span data-ttu-id="50b5f-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="50b5f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="50b5f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="50b5f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="50b5f-105">Возвращает сумму (объединение) двух входных значений.</span><span class="sxs-lookup"><span data-stu-id="50b5f-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="50b5f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="50b5f-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="50b5f-107">a: "Element []</span><span class="sxs-lookup"><span data-stu-id="50b5f-107">a : 'Element[]</span></span>

<span data-ttu-id="50b5f-108">Первый входной $a $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="50b5f-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="50b5f-109">b: ' element []</span><span class="sxs-lookup"><span data-stu-id="50b5f-109">b : 'Element[]</span></span>

<span data-ttu-id="50b5f-110">Второй входной $b $ для суммирования.</span><span class="sxs-lookup"><span data-stu-id="50b5f-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="50b5f-111">Выходные данные: ' element []</span><span class="sxs-lookup"><span data-stu-id="50b5f-111">Output : 'Element[]</span></span>

<span data-ttu-id="50b5f-112">Сумма $a + b $.</span><span class="sxs-lookup"><span data-stu-id="50b5f-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="50b5f-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="50b5f-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="50b5f-114">' Элемент</span><span class="sxs-lookup"><span data-stu-id="50b5f-114">'Element</span></span>

<span data-ttu-id="50b5f-115">Тип каждого элемента в каждом из двух входных массивов.</span><span class="sxs-lookup"><span data-stu-id="50b5f-115">The type of each element in each of the two input arrays.</span></span>