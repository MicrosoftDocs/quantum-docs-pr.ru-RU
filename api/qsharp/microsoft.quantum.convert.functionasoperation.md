---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Функция Функтионасоператион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 10703818242cf6b3853f08a45bfb9094f397f6c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224383"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="8009e-102">Функция Функтионасоператион</span><span class="sxs-lookup"><span data-stu-id="8009e-102">FunctionAsOperation function</span></span>

<span data-ttu-id="8009e-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="8009e-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="8009e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8009e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8009e-105">Преобразует функции в операции.</span><span class="sxs-lookup"><span data-stu-id="8009e-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="8009e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8009e-106">Description</span></span>

<span data-ttu-id="8009e-107">При наличии функции возвращает операцию, которая вызывает эту функцию и не выполняет никаких других действий.</span><span class="sxs-lookup"><span data-stu-id="8009e-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="8009e-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8009e-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="8009e-109">FN: "входные данные >"</span><span class="sxs-lookup"><span data-stu-id="8009e-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="8009e-110">Функция, которую необходимо преобразовать в операцию.</span><span class="sxs-lookup"><span data-stu-id="8009e-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="8009e-111">Выходные данные: input => ' Output</span><span class="sxs-lookup"><span data-stu-id="8009e-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="8009e-112">Операция `op` , которая `op(input)` идентична для `fn(input)` All `input` .</span><span class="sxs-lookup"><span data-stu-id="8009e-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8009e-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8009e-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="8009e-114">' Input</span><span class="sxs-lookup"><span data-stu-id="8009e-114">'Input</span></span>

<span data-ttu-id="8009e-115">Тип входных данных функции для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8009e-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="8009e-116">' Output</span><span class="sxs-lookup"><span data-stu-id="8009e-116">'Output</span></span>

<span data-ttu-id="8009e-117">Тип выходных данных функции для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8009e-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="8009e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8009e-118">Remarks</span></span>

<span data-ttu-id="8009e-119">Это в основном полезно для передачи функций функциям или операциям, которые в качестве входных данных ожидает операцию.</span><span class="sxs-lookup"><span data-stu-id="8009e-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>