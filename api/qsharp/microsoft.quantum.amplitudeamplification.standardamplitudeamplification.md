---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: Функция Стандардамплитудеамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 18228d45c4df280b004c595a7b0f1e2a607b8b2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731929"
---
# <a name="standardamplitudeamplification-function"></a><span data-ttu-id="9ac3f-102">Функция Стандардамплитудеамплификатион</span><span class="sxs-lookup"><span data-stu-id="9ac3f-102">StandardAmplitudeAmplification function</span></span>

<span data-ttu-id="9ac3f-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="9ac3f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="9ac3f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9ac3f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9ac3f-105">Стандартный алгоритм усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="9ac3f-105">Standard Amplitude Amplification algorithm</span></span>

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9ac3f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ac3f-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="9ac3f-107">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ac3f-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ac3f-108">Число итераций $n $ о усилении амплитуды</span><span class="sxs-lookup"><span data-stu-id="9ac3f-108">Number of iterations $n$ of amplitude amplification</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="9ac3f-109">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="9ac3f-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="9ac3f-110">Единая база данных Oracle $A $, подготавливающая начальное состояние</span><span class="sxs-lookup"><span data-stu-id="9ac3f-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="9ac3f-111">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ac3f-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ac3f-112">Индекс для отметки кубит</span><span class="sxs-lookup"><span data-stu-id="9ac3f-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="9ac3f-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="9ac3f-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="9ac3f-114">Операция, реализующая стандартный алгоритм такта для усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="9ac3f-114">An operation that implements the standard amplitude amplification quantum algorithm</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac3f-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ac3f-115">Remarks</span></span>

<span data-ttu-id="9ac3f-116">Это стандартный алгоритм усиления амплитуды, полученный при выборе фаз отражения, вычисленных при `AmpAmpPhasesStandard` условии, что \Бегин{алигн} а\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} эта операция готовит состояние \бегин{алигн} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ Text {Target}} \_ s + \cdots\ket {0} \_ f \end{align} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируется в состоянии $ \ket {0} \_ f\ket {0} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="9ac3f-116">This is the standard amplitude amplification algorithm obtained by a choice of reflection phases computed by `AmpAmpPhasesStandard` Assuming that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} this operation prepares the state \begin{align} \operatorname{AmpAmpByOracle}\ket{0}\_{f}\ket{0}\_s= \sin((2n+1)\sin^{-1}(\lambda))\ket{1}\_f\ket{\text{target}}\_s + \cdots\ket{0}\_f \end{align} In most cases, `flagQubit` and `auxiliaryRegister` is initialized in the state $\ket{0}\_f\ket{0}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="9ac3f-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="9ac3f-117">References</span></span>

- [<span data-ttu-id="9ac3f-118">*G. Брассард, P. Хойер, M. Моска, A. касание*</span><span class="sxs-lookup"><span data-stu-id="9ac3f-118"> *G. Brassard, P. Hoyer, M. Mosca, A. Tapp* </span></span>](https://arxiv.org/abs/quant-ph/0005055)