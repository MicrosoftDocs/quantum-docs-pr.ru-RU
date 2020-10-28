---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Операция Апплидиагоналунитари
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 6ecacf6e4fe2c505036de208c8aeb5350e479e3c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729625"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="f7dc6-102">Операция Апплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="f7dc6-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="f7dc6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f7dc6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f7dc6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f7dc6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f7dc6-105">Применяет массив сложных фаз к числовым состояниям регистра Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="f7dc6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f7dc6-106">Description</span></span>

<span data-ttu-id="f7dc6-107">Эта операция реализует диагональное единое, которое применяет сложный этап $e ^ {i \ theta_j} $ в $n $-кубит номер состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="f7dc6-108">В частности, эта операция может быть представлена единой</span><span class="sxs-lookup"><span data-stu-id="f7dc6-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="f7dc6-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \кет{ж}\бра{ж}.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="f7dc6-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="f7dc6-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="f7dc6-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f7dc6-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="f7dc6-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f7dc6-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f7dc6-113">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="f7dc6-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="f7dc6-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f7dc6-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f7dc6-116">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7dc6-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7dc6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f7dc6-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="f7dc6-118">Remarks</span></span>

<span data-ttu-id="f7dc6-119">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="f7dc6-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="f7dc6-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f7dc6-120">References</span></span>

- <span data-ttu-id="f7dc6-121">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="f7dc6-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="f7dc6-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="f7dc6-122">See Also</span></span>

- [<span data-ttu-id="f7dc6-123">Microsoft. тактов. Canon. Аппроксимателяпплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="f7dc6-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)