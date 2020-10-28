---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Операция Апплитранспоситион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733937"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="9caa8-102">Операция Апплитранспоситион</span><span class="sxs-lookup"><span data-stu-id="9caa8-102">ApplyTransposition operation</span></span>

<span data-ttu-id="9caa8-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="9caa8-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="9caa8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9caa8-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="9caa8-105">Описание</span><span class="sxs-lookup"><span data-stu-id="9caa8-105">Description</span></span>

<span data-ttu-id="9caa8-106">Эта операция меняет местами амплитуду с индексом на `a` амплитуду по индексу `b` в заданном векторе состояния `register` длины $n $.</span><span class="sxs-lookup"><span data-stu-id="9caa8-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="9caa8-107">Если `a` равно `b` , вектор состояния не изменяется.</span><span class="sxs-lookup"><span data-stu-id="9caa8-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="9caa8-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9caa8-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="9caa8-109">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9caa8-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9caa8-110">Первый индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="9caa8-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="9caa8-111">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9caa8-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9caa8-112">Второй индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="9caa8-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="9caa8-113">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9caa8-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9caa8-114">Список $n $ Кубитс, к которому применяется транспоситион.</span><span class="sxs-lookup"><span data-stu-id="9caa8-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9caa8-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9caa8-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

