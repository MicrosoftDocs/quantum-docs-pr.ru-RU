---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Операция Апплитранспоситион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203320"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="a2682-102">Операция Апплитранспоситион</span><span class="sxs-lookup"><span data-stu-id="a2682-102">ApplyTransposition operation</span></span>

<span data-ttu-id="a2682-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="a2682-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="a2682-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2682-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a2682-105">Описание</span><span class="sxs-lookup"><span data-stu-id="a2682-105">Description</span></span>

<span data-ttu-id="a2682-106">Эта операция меняет местами амплитуду с индексом на `a` амплитуду по индексу `b` в заданном векторе состояния `register` длины $n $.</span><span class="sxs-lookup"><span data-stu-id="a2682-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="a2682-107">Если `a` равно `b` , вектор состояния не изменяется.</span><span class="sxs-lookup"><span data-stu-id="a2682-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="a2682-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a2682-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a2682-109">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a2682-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a2682-110">Первый индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="a2682-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="a2682-111">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a2682-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a2682-112">Второй индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="a2682-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="a2682-113">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a2682-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a2682-114">Список $n $ Кубитс, к которому применяется транспоситион.</span><span class="sxs-lookup"><span data-stu-id="a2682-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2682-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2682-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

