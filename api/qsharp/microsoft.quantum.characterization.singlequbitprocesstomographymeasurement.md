---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Операция Синглекубитпроцесстомографимеасуремент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 34e5143d5be316ee42a63124d35475949db0a692
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714922"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="d3ba3-102">Операция Синглекубитпроцесстомографимеасуремент</span><span class="sxs-lookup"><span data-stu-id="d3ba3-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="d3ba3-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="d3ba3-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="d3ba3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3ba3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3ba3-105">Выполняет кубит процесс томографи измерения на основе Паули, учитывая конкретный интересующий Вас канал.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="d3ba3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3ba3-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="d3ba3-107">подготовка: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d3ba3-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d3ba3-108">Элемент Паули базиса $P $, в котором подготавливается кубит.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="d3ba3-109">Измерение: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d3ba3-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d3ba3-110">Элемент Паули базиса $Q $, в котором измеряется кубит.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="d3ba3-111">канал: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [единица](xref:microsoft.quantum.lang-ref.unit) кубит</span><span class="sxs-lookup"><span data-stu-id="d3ba3-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d3ba3-112">Один канал кубит $ \Ламбда $, поведение которого оценивается с помощью процесса томографи.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d3ba3-113">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="d3ba3-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="d3ba3-114">Результат `Zero` с вероятностью $ $ \Бегин{алигн} \пр (\тексттт{зеро} | \ламбда; P, Q) = \Операторнаме{ТР}\лефт (\фрак{\болдоне + Q} {2} \ламбда\лефт [\фрак{\болдоне + P} {2} \ригхт] \ригхт).</span><span class="sxs-lookup"><span data-stu-id="d3ba3-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="d3ba3-115">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="d3ba3-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ba3-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3ba3-116">Remarks</span></span>

<span data-ttu-id="d3ba3-117">Распределение по результатам, возвращаемым этой операцией, является особым случаем для двух кубит состояния томографи.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="d3ba3-118">Let $ \рхо = J (\Ламбда)/$2 должно быть Чои – Жамиłковски для $ \Ламбда $.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="d3ba3-119">Затем приведенный выше дистрибутив идентичен $ $ \бегин{алигн} \Пр (\Тексттт{зеро} | \рхо; M) = \Операторнаме{ТР} (M \рхо), \енд{алигн} $ $ WHERE $M = 2 (\болдоне + P) ^ \Масрм{т}/2 \кдот (\болдоне + Q)/$2 — это эффективное измерение, соответствующее $P $ и $Q $.</span><span class="sxs-lookup"><span data-stu-id="d3ba3-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>