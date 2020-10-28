---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Операция Естиматефрекуенциа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 88f0a237975c158bffcc015f79d2134b210ce83b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715062"
---
# <a name="estimatefrequencya-operation"></a><span data-ttu-id="956b5-102">Операция Естиматефрекуенциа</span><span class="sxs-lookup"><span data-stu-id="956b5-102">EstimateFrequencyA operation</span></span>

<span data-ttu-id="956b5-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="956b5-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="956b5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="956b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="956b5-105">Учитывая аджоинтабле и измерение подготовки, вы оцениваете частоту, с которой измерение завершается (Возвращает `Zero` ), выполняя заданное число испытаний.</span><span class="sxs-lookup"><span data-stu-id="956b5-105">Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="956b5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="956b5-106">Input</span></span>

### <a name="preparation--qubit--unit-adj"></a><span data-ttu-id="956b5-107">подготовка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="956b5-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="956b5-108">Операция аджоинтабле $P $, которая подготавливает заданное состояние $ \рхо $ к входному регистру.</span><span class="sxs-lookup"><span data-stu-id="956b5-108">An adjointable operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="956b5-109">Измерение: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = __недопустимый <Result>__ ></span><span class="sxs-lookup"><span data-stu-id="956b5-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="956b5-110">Операция $M $, представляющая интересующую вас единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="956b5-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="956b5-111">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="956b5-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="956b5-112">Количество Кубитс, для которых каждый из них является подготовительным и измеряется.</span><span class="sxs-lookup"><span data-stu-id="956b5-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="956b5-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="956b5-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="956b5-114">Количество случаев, когда измерение должно быть выполнено, чтобы оценить интересующую вас частоту.</span><span class="sxs-lookup"><span data-stu-id="956b5-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="956b5-115">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="956b5-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="956b5-116">Оценка $ \хат{п} $ частоты, с которой $M (P (\ket{00 \кдотс 0} \bra{00 \кдотс 0})) $ Returns `Zero` , полученный с помощью несмещенного биномиальное оценщика $ \хат{п} = n \_ {\упарров}/n \_ {\текст{меасурементс}} $, где $n \_ {\упарров} $ — это количество `Zero` наблюдаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="956b5-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="956b5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="956b5-117">Remarks</span></span>

<span data-ttu-id="956b5-118">Для операций аджоинтабле определенные предположения, такие как вызов операции, будут подготавливать Кубитс в точно такое же состояние, что позволит целевым компьютерам выполнять оптимизацию производительности.</span><span class="sxs-lookup"><span data-stu-id="956b5-118">For adjointable operations, certain assumptions can be made such like calling the operation will prepare the qubits to exactly the same state, which allow target machines to make some performance optimizations.</span></span>