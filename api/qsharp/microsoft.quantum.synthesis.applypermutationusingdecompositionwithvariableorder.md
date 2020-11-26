---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Операция Апплипермутатионусингдекомпоситионвисвариаблеордер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: a5ca9b366f7ff477070e21fea047ff04b425439c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203439"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="5b366-102">Операция Апплипермутатионусингдекомпоситионвисвариаблеордер</span><span class="sxs-lookup"><span data-stu-id="5b366-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="5b366-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5b366-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5b366-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b366-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b366-105">Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="5b366-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5b366-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5b366-106">Description</span></span>

<span data-ttu-id="5b366-107">Эта операция является более общей версией, @"microsoft.quantum.synthesis.applypermutationusingdecomposition" в которой можно указать порядок переменных.</span><span class="sxs-lookup"><span data-stu-id="5b366-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="5b366-108">Другой порядок переменных изменяет последовательность декомпозиции и таблицы истинности, используемые для управляемых @"microsoft.quantum.intrinsic.x" шлюзов.</span><span class="sxs-lookup"><span data-stu-id="5b366-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="5b366-109">Поэтому при изменении порядка переменных изменяется количество общих шлюзов, используемых для реализации перестановки.</span><span class="sxs-lookup"><span data-stu-id="5b366-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="5b366-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b366-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="5b366-111">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5b366-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5b366-112">Перестановка элементов $2 ^ n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="5b366-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="5b366-113">Вариаблеордер: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5b366-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5b366-114">Перестановка элементов $n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="5b366-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="5b366-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b366-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5b366-116">Список $n $ Кубитс, к которому применяется перестановка.</span><span class="sxs-lookup"><span data-stu-id="5b366-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b366-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b366-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5b366-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="5b366-118">See Also</span></span>

- [<span data-ttu-id="5b366-119">Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситион</span><span class="sxs-lookup"><span data-stu-id="5b366-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="5b366-120">Microsoft. тактов. синтез. Апплипермутатионусингтрансформатион</span><span class="sxs-lookup"><span data-stu-id="5b366-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)