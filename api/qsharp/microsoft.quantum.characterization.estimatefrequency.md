---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Операция Естиматефрекуенци
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 30b21a8e86eb5a4dd8dd8207dbdc6a0970308319
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216257"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="d7155-102">Операция Естиматефрекуенци</span><span class="sxs-lookup"><span data-stu-id="d7155-102">EstimateFrequency operation</span></span>

<span data-ttu-id="d7155-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="d7155-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="d7155-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d7155-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d7155-105">При подготовке и измерении оценивается частота, с которой измерение завершается (Возвращает `Zero` ), выполняя заданное число испытаний.</span><span class="sxs-lookup"><span data-stu-id="d7155-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="d7155-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d7155-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="d7155-107">подготовка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="d7155-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d7155-108">Операция $P $, которая подготавливает заданное состояние $ \рхо $ к входному регистру.</span><span class="sxs-lookup"><span data-stu-id="d7155-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="d7155-109">Измерение: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = __недопустимый <Result>__></span><span class="sxs-lookup"><span data-stu-id="d7155-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="d7155-110">Операция $M $, представляющая интересующую вас единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="d7155-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="d7155-111">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7155-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d7155-112">Количество Кубитс, для которых каждый из них является подготовительным и измеряется.</span><span class="sxs-lookup"><span data-stu-id="d7155-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="d7155-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7155-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d7155-114">Количество случаев, когда измерение должно быть выполнено, чтобы оценить интересующую вас частоту.</span><span class="sxs-lookup"><span data-stu-id="d7155-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="d7155-115">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7155-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7155-116">Оценка $ \хат{п} $ частоты, с которой $M (P (\ket{00 \кдотс 0} \bra{00 \кдотс 0})) $ Returns `Zero` , полученный с помощью несмещенного биномиальное оценщика $ \хат{п} = n \_ {\упарров}/n \_ {\текст{меасурементс}} $, где $n \_ {\упарров} $ — это количество `Zero` наблюдаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="d7155-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="d7155-117">Это особенно важно на целевых компьютерах, которые действуют с учетом физических ограничений, что не позволяет измерять вероятности.</span><span class="sxs-lookup"><span data-stu-id="d7155-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>