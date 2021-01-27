---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Операция Робустфасистиматион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851803"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="7711b-102">Операция Робустфасистиматион</span><span class="sxs-lookup"><span data-stu-id="7711b-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="7711b-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="7711b-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="7711b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7711b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7711b-105">Выполняет устойчивый алгоритм оценки неитеративного тактового этапа для заданных Oracle `U` и еиженстате и предоставляет единую оценку этапа с масштабированием в пределах Гейзенбега.</span><span class="sxs-lookup"><span data-stu-id="7711b-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="7711b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7711b-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="7711b-107">БитспреЦисион: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7711b-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7711b-108">Это дает оценку $ \фи $ со стандартным отклонением $ \сигма \ле 2 \ PI/2 ^ \Текст{битспреЦисион} $ с помощью такого количества запросов, как $ \сигма \ле 10,7 \пи/\текст{# запросов} $.</span><span class="sxs-lookup"><span data-stu-id="7711b-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="7711b-109">Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="7711b-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="7711b-110">Операция, реализующая $U ^ m $ для заданного целого числа, включает $m $.</span><span class="sxs-lookup"><span data-stu-id="7711b-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="7711b-111">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7711b-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7711b-112">Регистр такта, в котором $U $ действует.</span><span class="sxs-lookup"><span data-stu-id="7711b-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="7711b-113">Если в нем хранится еиженстате $ \кет{\фи} $ of $U $, то $U \кет{\фи} = e ^ {и\фи} \кет{\фи} $ for $ \фи\ин (-\пи, \пи] $ Неизвестный этап.</span><span class="sxs-lookup"><span data-stu-id="7711b-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="7711b-114">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7711b-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="7711b-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="7711b-115">Remarks</span></span>

<span data-ttu-id="7711b-116">В ограничении большого количества запросов Cramer-Rao нижние границы для стандартного отклонения от оценки $ \фи $ удовлетворяет $ \сигма \же 2 \пи/\текст{# запросов} $.</span><span class="sxs-lookup"><span data-stu-id="7711b-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="7711b-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="7711b-117">References</span></span>

- <span data-ttu-id="7711b-118">Надежная калибровка универсального Single-Qubit Gate-Set с помощью надежной оценки этапа Шелби Киммел, Guang Хао Low, текста книги J. Йодер https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="7711b-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>