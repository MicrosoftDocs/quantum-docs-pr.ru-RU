---
uid: Microsoft.Quantum.Convert.Call
title: Операция вызова
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850196"
---
# <a name="call-operation"></a><span data-ttu-id="a35a8-102">Операция вызова</span><span class="sxs-lookup"><span data-stu-id="a35a8-102">Call operation</span></span>

<span data-ttu-id="a35a8-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="a35a8-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="a35a8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a35a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a35a8-105">Вызывает функцию с заданным входным параметром.</span><span class="sxs-lookup"><span data-stu-id="a35a8-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="a35a8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a35a8-106">Description</span></span>

<span data-ttu-id="a35a8-107">При наличии функции и входных данных для этой функции вызывает функцию и возвращает ее выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a35a8-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="a35a8-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a35a8-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="a35a8-109">FN: "входные данные >"</span><span class="sxs-lookup"><span data-stu-id="a35a8-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="a35a8-110">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="a35a8-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="a35a8-111">входные данные: "входные данные</span><span class="sxs-lookup"><span data-stu-id="a35a8-111">input : 'Input</span></span>

<span data-ttu-id="a35a8-112">Входные данные, передаваемые в функцию.</span><span class="sxs-lookup"><span data-stu-id="a35a8-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="a35a8-113">Выходные данные: "Output</span><span class="sxs-lookup"><span data-stu-id="a35a8-113">Output : 'Output</span></span>

<span data-ttu-id="a35a8-114">Результат вызова метода `fn`.</span><span class="sxs-lookup"><span data-stu-id="a35a8-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a35a8-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a35a8-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="a35a8-116">' Input</span><span class="sxs-lookup"><span data-stu-id="a35a8-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="a35a8-117">' Output</span><span class="sxs-lookup"><span data-stu-id="a35a8-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="a35a8-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="a35a8-118">Remarks</span></span>

<span data-ttu-id="a35a8-119">Эта операция в основном полезна для принудительного вызова функции в определенном месте операции или для вызова функции, в которой ожидается операция.</span><span class="sxs-lookup"><span data-stu-id="a35a8-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>