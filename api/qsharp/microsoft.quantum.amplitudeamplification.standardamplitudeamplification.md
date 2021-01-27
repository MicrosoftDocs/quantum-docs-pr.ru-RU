---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: Функция Стандардамплитудеамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 984bfee89b6d79750228b8ca6aaf404f58aecd41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843926"
---
# <a name="standardamplitudeamplification-function"></a><span data-ttu-id="5d220-102">Функция Стандардамплитудеамплификатион</span><span class="sxs-lookup"><span data-stu-id="5d220-102">StandardAmplitudeAmplification function</span></span>

<span data-ttu-id="5d220-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="5d220-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="5d220-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d220-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d220-105">Стандартный алгоритм усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="5d220-105">Standard Amplitude Amplification algorithm</span></span>

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="5d220-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d220-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="5d220-107">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d220-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d220-108">Число итераций $n $ о усилении амплитуды</span><span class="sxs-lookup"><span data-stu-id="5d220-108">Number of iterations $n$ of amplitude amplification</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="5d220-109">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="5d220-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="5d220-110">Единая база данных Oracle $A $, подготавливающая начальное состояние</span><span class="sxs-lookup"><span data-stu-id="5d220-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="5d220-111">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d220-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d220-112">Индекс для отметки кубит</span><span class="sxs-lookup"><span data-stu-id="5d220-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="5d220-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="5d220-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5d220-114">Операция, реализующая стандартный алгоритм такта для усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="5d220-114">An operation that implements the standard amplitude amplification quantum algorithm</span></span>

## <a name="remarks"></a><span data-ttu-id="5d220-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d220-115">Remarks</span></span>

<span data-ttu-id="5d220-116">Это стандартный алгоритм усиления амплитуды, полученный при выборе фаз отражения, вычисленных при `AmpAmpPhasesStandard` условии, что \Бегин{алигн} а\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} эта операция готовит состояние \бегин{алигн} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ Text {Target}} \_ s + \cdots\ket {0} \_ f \end{align} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируется в состоянии $ \ket {0} \_ f\ket {0} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="5d220-116">This is the standard amplitude amplification algorithm obtained by a choice of reflection phases computed by `AmpAmpPhasesStandard` Assuming that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} this operation prepares the state \begin{align} \operatorname{AmpAmpByOracle}\ket{0}\_{f}\ket{0}\_s= \sin((2n+1)\sin^{-1}(\lambda))\ket{1}\_f\ket{\text{target}}\_s + \cdots\ket{0}\_f \end{align} In most cases, `flagQubit` and `auxiliaryRegister` is initialized in the state $\ket{0}\_f\ket{0}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="5d220-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="5d220-117">References</span></span>

- [<span data-ttu-id="5d220-118">*G. Брассард, P. Хойер, M. Моска, A. касание*</span><span class="sxs-lookup"><span data-stu-id="5d220-118"> *G. Brassard, P. Hoyer, M. Mosca, A. Tapp* </span></span>](https://arxiv.org/abs/quant-ph/0005055)