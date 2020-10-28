---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Операция Апплипермутатионусингдекомпоситионвисвариаблеордер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733960"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="1465c-102">Операция Апплипермутатионусингдекомпоситионвисвариаблеордер</span><span class="sxs-lookup"><span data-stu-id="1465c-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="1465c-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1465c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1465c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1465c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1465c-105">Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="1465c-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="1465c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1465c-106">Description</span></span>

<span data-ttu-id="1465c-107">Эта операция является более общей версией, @"microsoft.quantum.synthesis.applypermutationusingdecomposition" в которой можно указать порядок переменных.</span><span class="sxs-lookup"><span data-stu-id="1465c-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="1465c-108">Другой порядок переменных изменяет последовательность декомпозиции и таблицы истинности, используемые для управляемых @"microsoft.quantum.intrinsic.x" шлюзов.</span><span class="sxs-lookup"><span data-stu-id="1465c-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="1465c-109">Поэтому при изменении порядка переменных изменяется количество общих шлюзов, используемых для реализации перестановки.</span><span class="sxs-lookup"><span data-stu-id="1465c-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="1465c-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1465c-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="1465c-111">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1465c-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1465c-112">Перестановка элементов $2 ^ n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="1465c-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="1465c-113">Вариаблеордер: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1465c-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1465c-114">Перестановка элементов $n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="1465c-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="1465c-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1465c-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1465c-116">Список $n $ Кубитс, к которому применяется перестановка.</span><span class="sxs-lookup"><span data-stu-id="1465c-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1465c-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1465c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1465c-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="1465c-118">See Also</span></span>

- [<span data-ttu-id="1465c-119">Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситион</span><span class="sxs-lookup"><span data-stu-id="1465c-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="1465c-120">Microsoft. тактов. синтез. Апплипермутатионусингтрансформатион</span><span class="sxs-lookup"><span data-stu-id="1465c-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)