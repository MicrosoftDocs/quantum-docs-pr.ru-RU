---
uid: Microsoft.Quantum.Convert.Call
title: Операция вызова
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 92c159cef878fb587b0ed514fd6660dd19527cab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214217"
---
# <a name="call-operation"></a><span data-ttu-id="b3d35-102">Операция вызова</span><span class="sxs-lookup"><span data-stu-id="b3d35-102">Call operation</span></span>

<span data-ttu-id="b3d35-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="b3d35-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="b3d35-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3d35-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3d35-105">Вызывает функцию с заданным входным параметром.</span><span class="sxs-lookup"><span data-stu-id="b3d35-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="b3d35-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b3d35-106">Description</span></span>

<span data-ttu-id="b3d35-107">При наличии функции и входных данных для этой функции вызывает функцию и возвращает ее выходные данные.</span><span class="sxs-lookup"><span data-stu-id="b3d35-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="b3d35-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3d35-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="b3d35-109">FN: "входные данные >"</span><span class="sxs-lookup"><span data-stu-id="b3d35-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="b3d35-110">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="b3d35-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="b3d35-111">входные данные: "входные данные</span><span class="sxs-lookup"><span data-stu-id="b3d35-111">input : 'Input</span></span>

<span data-ttu-id="b3d35-112">Входные данные, передаваемые в функцию.</span><span class="sxs-lookup"><span data-stu-id="b3d35-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="b3d35-113">Выходные данные: "Output</span><span class="sxs-lookup"><span data-stu-id="b3d35-113">Output : 'Output</span></span>

<span data-ttu-id="b3d35-114">Результат вызова метода `fn`.</span><span class="sxs-lookup"><span data-stu-id="b3d35-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b3d35-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b3d35-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="b3d35-116">' Input</span><span class="sxs-lookup"><span data-stu-id="b3d35-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="b3d35-117">' Output</span><span class="sxs-lookup"><span data-stu-id="b3d35-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="b3d35-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3d35-118">Remarks</span></span>

<span data-ttu-id="b3d35-119">Эта операция в основном полезна для принудительного вызова функции в определенном месте операции или для вызова функции, в которой ожидается операция.</span><span class="sxs-lookup"><span data-stu-id="b3d35-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>