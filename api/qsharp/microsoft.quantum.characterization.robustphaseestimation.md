---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Операция Робустфасистиматион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 3e6774e2fe348668840cdc08fe3a070ec3d82a6d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216087"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="b4069-102">Операция Робустфасистиматион</span><span class="sxs-lookup"><span data-stu-id="b4069-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="b4069-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="b4069-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="b4069-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4069-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4069-105">Выполняет устойчивый алгоритм оценки неитеративного тактового этапа для заданных Oracle `U` и еиженстате и предоставляет единую оценку этапа с масштабированием в пределах Гейзенбега.</span><span class="sxs-lookup"><span data-stu-id="b4069-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="b4069-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b4069-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="b4069-107">БитспреЦисион: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b4069-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b4069-108">Это дает оценку $ \фи $ со стандартным отклонением $ \сигма \ле 2 \ PI/2 ^ \Текст{битспреЦисион} $ с помощью такого количества запросов, как $ \сигма \ле 10,7 \пи/\текст{# запросов} $.</span><span class="sxs-lookup"><span data-stu-id="b4069-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="b4069-109">Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="b4069-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="b4069-110">Операция, реализующая $U ^ m $ для заданного целого числа, включает $m $.</span><span class="sxs-lookup"><span data-stu-id="b4069-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="b4069-111">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b4069-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b4069-112">Регистр такта, в котором $U $ действует.</span><span class="sxs-lookup"><span data-stu-id="b4069-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="b4069-113">Если в нем хранится еиженстате $ \кет{\фи} $ of $U $, то $U \кет{\фи} = e ^ {и\фи} \кет{\фи} $ for $ \фи\ин (-\пи, \пи] $ Неизвестный этап.</span><span class="sxs-lookup"><span data-stu-id="b4069-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="b4069-114">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b4069-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="b4069-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4069-115">Remarks</span></span>

<span data-ttu-id="b4069-116">В ограничении большого количества запросов Cramer-Rao нижние границы для стандартного отклонения от оценки $ \фи $ удовлетворяет $ \сигма \же 2 \пи/\текст{# запросов} $.</span><span class="sxs-lookup"><span data-stu-id="b4069-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="b4069-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="b4069-117">References</span></span>

- <span data-ttu-id="b4069-118">Надежная калибровка универсального Single-Qubit Gate-Set с помощью надежной оценки этапа Шелби Киммел, Guang Хао Low, текста книги J. Йодер https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="b4069-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>