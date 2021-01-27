---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: Операция Аппроксимателяпплидиагоналунитари
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 5d8f6646c124f4296b9cd2abd71e73de5a530e55
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850332"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a><span data-ttu-id="4ebba-102">Операция Аппроксимателяпплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="4ebba-102">ApproximatelyApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="4ebba-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4ebba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4ebba-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ebba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ebba-105">Применяет массив сложных фаз к числовым состояниям регистра Кубитс, сокращая небольшие углы вращения в соответствии с заданным отклонением.</span><span class="sxs-lookup"><span data-stu-id="4ebba-105">Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4ebba-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4ebba-106">Description</span></span>

<span data-ttu-id="4ebba-107">Эта операция реализует диагональное единое, которое применяет сложный этап $e ^ {i \ theta_j} $ в $n $-кубит номер состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="4ebba-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="4ebba-108">В частности, эта операция может быть представлена единой</span><span class="sxs-lookup"><span data-stu-id="4ebba-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="4ebba-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \кет{ж}\бра{ж}.</span><span class="sxs-lookup"><span data-stu-id="4ebba-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="4ebba-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="4ebba-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="4ebba-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4ebba-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="4ebba-112">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4ebba-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4ebba-113">Допуск, ниже которого усекаются небольшие коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="4ebba-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="4ebba-114">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4ebba-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4ebba-115">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="4ebba-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="4ebba-116">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4ebba-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="4ebba-117">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4ebba-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4ebba-118">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4ebba-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4ebba-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4ebba-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4ebba-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="4ebba-120">Remarks</span></span>

<span data-ttu-id="4ebba-121">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="4ebba-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="4ebba-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="4ebba-122">References</span></span>

- <span data-ttu-id="4ebba-123">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="4ebba-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="4ebba-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="4ebba-124">See Also</span></span>

- [<span data-ttu-id="4ebba-125">Microsoft. тактов. Canon. Апплидиагоналунитари</span><span class="sxs-lookup"><span data-stu-id="4ebba-125">Microsoft.Quantum.Canon.ApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)