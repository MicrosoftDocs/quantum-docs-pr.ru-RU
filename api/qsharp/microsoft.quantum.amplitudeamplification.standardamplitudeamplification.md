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
# <a name="standardamplitudeamplification-function"></a>Функция Стандардамплитудеамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Стандартный алгоритм усиления амплитуды

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="niterations--int"></a>Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)

Число итераций $n $ о усилении амплитуды


### <a name="stateoracle--stateoracle"></a>Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)

Единая база данных Oracle $A $, подготавливающая начальное состояние


### <a name="idxflagqubit--int"></a>Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)

Индекс для отметки кубит



## <a name="output--qubit--unit-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Операция, реализующая стандартный алгоритм такта для усиления амплитуды

## <a name="remarks"></a>Remarks

Это стандартный алгоритм усиления амплитуды, полученный при выборе фаз отражения, вычисленных при `AmpAmpPhasesStandard` условии, что \Бегин{алигн} а\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} эта операция готовит состояние \бегин{алигн} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ Text {Target}} \_ s + \cdots\ket {0} \_ f \end{align} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируется в состоянии $ \ket {0} \_ f\ket {0} \_ a $.

## <a name="references"></a>Ссылки

- [*G. Брассард, P. Хойер, M. Моска, A. касание*](https://arxiv.org/abs/quant-ph/0005055)