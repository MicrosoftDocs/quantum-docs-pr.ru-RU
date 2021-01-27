---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Операция Апплипермутатионусингтрансформатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: 79913bec44514d477b7ee0668b43396b297b9ab8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858998"
---
# <a name="applypermutationusingtransformation-operation"></a><span data-ttu-id="39a30-102">Операция Апплипермутатионусингтрансформатион</span><span class="sxs-lookup"><span data-stu-id="39a30-102">ApplyPermutationUsingTransformation operation</span></span>

<span data-ttu-id="39a30-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="39a30-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="39a30-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39a30-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39a30-105">Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе преобразования.</span><span class="sxs-lookup"><span data-stu-id="39a30-105">Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="39a30-106">Описание</span><span class="sxs-lookup"><span data-stu-id="39a30-106">Description</span></span>

<span data-ttu-id="39a30-107">Эта процедура реализует метод синтеза на основе однонаправленного преобразования.</span><span class="sxs-lookup"><span data-stu-id="39a30-107">This procedure implements the unidirectional transformation based synthesis approach.</span></span>  <span data-ttu-id="39a30-108">Входные данные — это перестановка $ \пи $ over $2 ^ n $ Elements $ \{ 0, \дотс, 2 ^ n-1 \} $, представляющая $n $-Variable обратимая логическая функция.</span><span class="sxs-lookup"><span data-stu-id="39a30-108">Input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="39a30-109">Алгоритм последовательно выполняет следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="39a30-109">The algorithm performs iteratively the following steps:</span></span>

1. <span data-ttu-id="39a30-110">Найдите наименьшее $x $ например, $x \не \пи (x) = y $.</span><span class="sxs-lookup"><span data-stu-id="39a30-110">Find smallest $x$ such that $x \ne \pi(x) = y$.</span></span>
2. <span data-ttu-id="39a30-111">Поиск нескольких управляемых операций Тоффоли, которые применяются к выходам, делают $ \пи (x) = x $ и не изменяют $ \пи (x ') $ для всех $x "< x $</span><span class="sxs-lookup"><span data-stu-id="39a30-111">Find multiple-controlled Toffoli operations, which applied to the outputs make $\pi(x) = x$ and do not change $\pi(x')$ for all $x' < x$</span></span>

## <a name="input"></a><span data-ttu-id="39a30-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="39a30-112">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="39a30-113">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="39a30-113">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="39a30-114">Перестановка элементов $2 ^ n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="39a30-114">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="39a30-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39a30-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39a30-116">Список $n $ Кубитс, к которому применяется перестановка.</span><span class="sxs-lookup"><span data-stu-id="39a30-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39a30-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39a30-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="39a30-118">Пример</span><span class="sxs-lookup"><span data-stu-id="39a30-118">Example</span></span>

<span data-ttu-id="39a30-119">Для синтезирования `SWAP` операции выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="39a30-119">To synthesize a `SWAP` operation:</span></span>

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingTransformation([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a><span data-ttu-id="39a30-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="39a30-120">References</span></span>

- [<span data-ttu-id="39a30-121">*Г. Майкл Миллер*, *Дмитрий Маслов*, *жерхард W. дуекк*, proc. DAC 2003, IEEE, PP. 318-323, 2003</span><span class="sxs-lookup"><span data-stu-id="39a30-121">*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, Proc. DAC 2003, IEEE, pp. 318-323, 2003</span></span>](https://doi.org/10.1145/775832.775915)
- [<span data-ttu-id="39a30-122">*Матиас соекен*, *Жерхард W. дуекк*, *D. Майкл миллер*, proc. RC 2016, springer link, PP. 307-321, 2016</span><span class="sxs-lookup"><span data-stu-id="39a30-122">*Mathias Soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, Proc. RC 2016, Springer, pp. 307-321, 2016</span></span>](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a><span data-ttu-id="39a30-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="39a30-123">See Also</span></span>

- [<span data-ttu-id="39a30-124">Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситион</span><span class="sxs-lookup"><span data-stu-id="39a30-124">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)