---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Функция Висзероинсертедат
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 6e13251741dadb19740b208cdfc13a14964a48dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733880"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="b447c-102">Функция Висзероинсертедат</span><span class="sxs-lookup"><span data-stu-id="b447c-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="b447c-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b447c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b447c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b447c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b447c-105">Вставить 0-разрядное значение в целое число</span><span class="sxs-lookup"><span data-stu-id="b447c-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="b447c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b447c-106">Description</span></span>

<span data-ttu-id="b447c-107">Эта операция принимает целое число, вставляет 0 в бит `position` и возвращает обновленное значение в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="b447c-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="b447c-108">Например, при вставке значения 0 в позиции 2 в номере 10 (10 долл. {10} = 1010_ {2} $) возвращается число 18 ($18 _ {10} = 10010_ {2} $).</span><span class="sxs-lookup"><span data-stu-id="b447c-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="b447c-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b447c-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="b447c-110">Расположение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b447c-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b447c-111">Позиции, в которую вставляется 0</span><span class="sxs-lookup"><span data-stu-id="b447c-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="b447c-112">значение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b447c-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b447c-113">Изменяемое значение</span><span class="sxs-lookup"><span data-stu-id="b447c-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="b447c-114">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b447c-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b447c-115">Измененное значение</span><span class="sxs-lookup"><span data-stu-id="b447c-115">Modified value</span></span>