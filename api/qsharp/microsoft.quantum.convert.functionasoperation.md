---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Функция Функтионасоператион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713508"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="5b68f-102">Функция Функтионасоператион</span><span class="sxs-lookup"><span data-stu-id="5b68f-102">FunctionAsOperation function</span></span>

<span data-ttu-id="5b68f-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="5b68f-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="5b68f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b68f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b68f-105">Преобразует функции в операции.</span><span class="sxs-lookup"><span data-stu-id="5b68f-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="5b68f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5b68f-106">Description</span></span>

<span data-ttu-id="5b68f-107">При наличии функции возвращает операцию, которая вызывает эту функцию и не выполняет никаких других действий.</span><span class="sxs-lookup"><span data-stu-id="5b68f-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="5b68f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b68f-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="5b68f-109">FN: "входные данные >"</span><span class="sxs-lookup"><span data-stu-id="5b68f-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="5b68f-110">Функция, которую необходимо преобразовать в операцию.</span><span class="sxs-lookup"><span data-stu-id="5b68f-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="5b68f-111">Выходные данные: input => ' Output</span><span class="sxs-lookup"><span data-stu-id="5b68f-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="5b68f-112">Операция `op` , которая `op(input)` идентична для `fn(input)` All `input` .</span><span class="sxs-lookup"><span data-stu-id="5b68f-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5b68f-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5b68f-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="5b68f-114">' Input</span><span class="sxs-lookup"><span data-stu-id="5b68f-114">'Input</span></span>

<span data-ttu-id="5b68f-115">Тип входных данных функции для преобразования.</span><span class="sxs-lookup"><span data-stu-id="5b68f-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="5b68f-116">' Output</span><span class="sxs-lookup"><span data-stu-id="5b68f-116">'Output</span></span>

<span data-ttu-id="5b68f-117">Тип выходных данных функции для преобразования.</span><span class="sxs-lookup"><span data-stu-id="5b68f-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b68f-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="5b68f-118">Remarks</span></span>

<span data-ttu-id="5b68f-119">Это в основном полезно для передачи функций функциям или операциям, которые в качестве входных данных ожидает операцию.</span><span class="sxs-lookup"><span data-stu-id="5b68f-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>