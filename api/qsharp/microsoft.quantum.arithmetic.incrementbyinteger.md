---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Операция Инкрементбинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222972"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="ea622-102">Операция Инкрементбинтежер</span><span class="sxs-lookup"><span data-stu-id="ea622-102">IncrementByInteger operation</span></span>

<span data-ttu-id="ea622-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ea622-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ea622-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea622-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea622-105">Увеличивает значение регистра неподписанного такта на классическое целое число с использованием ротаций фазы.</span><span class="sxs-lookup"><span data-stu-id="ea622-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ea622-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ea622-106">Description</span></span>

<span data-ttu-id="ea622-107">Предположим, что `target` кодирует целое число без знака $x $ в кодировке с прямым порядком байтов и `increment` равно $a $.</span><span class="sxs-lookup"><span data-stu-id="ea622-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="ea622-108">Затем эта операция реализует единую $ \кет{КС} \мапсто \кет{КС + a} $, где сложение выполняется по модулю $2 ^ n $, где $n = \Тексттт{ленгс (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="ea622-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="ea622-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ea622-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="ea622-110">приращение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea622-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea622-111">Целое число, на которое `target` увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="ea622-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="ea622-112">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ea622-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ea622-113">Тактовый регистр кодирует целое число без знака, используя обратную кодировку с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ea622-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ea622-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea622-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

