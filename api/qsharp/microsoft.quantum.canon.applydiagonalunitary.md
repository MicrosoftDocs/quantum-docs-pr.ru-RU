---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Операция Апплидиагоналунитари
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 8f17c3cb222bef00ead5e7fea5d29d296b9a428a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218858"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="9d3e5-102">Операция Апплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="9d3e5-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="9d3e5-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d3e5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d3e5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d3e5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d3e5-105">Применяет массив сложных фаз к числовым состояниям регистра Кубитс.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="9d3e5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9d3e5-106">Description</span></span>

<span data-ttu-id="9d3e5-107">Эта операция реализует диагональное единое, которое применяет сложный этап $e ^ {i \ theta_j} $ в $n $-кубит номер состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="9d3e5-108">В частности, эта операция может быть представлена единой</span><span class="sxs-lookup"><span data-stu-id="9d3e5-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="9d3e5-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \кет{ж}\бра{ж}.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="9d3e5-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="9d3e5-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9d3e5-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9d3e5-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="9d3e5-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9d3e5-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9d3e5-113">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="9d3e5-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="9d3e5-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9d3e5-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9d3e5-116">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d3e5-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d3e5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9d3e5-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d3e5-118">Remarks</span></span>

<span data-ttu-id="9d3e5-119">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="9d3e5-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="9d3e5-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="9d3e5-120">References</span></span>

- <span data-ttu-id="9d3e5-121">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="9d3e5-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="9d3e5-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="9d3e5-122">See Also</span></span>

- [<span data-ttu-id="9d3e5-123">Microsoft. тактов. Canon. Аппроксимателяпплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="9d3e5-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)