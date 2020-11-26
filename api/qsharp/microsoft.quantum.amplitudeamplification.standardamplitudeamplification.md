---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: Функция Стандардамплитудеамплификатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 23a2b3dbe5ea404059994167f69e11458c0c22ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191182"
---
# <a name="standardamplitudeamplification-function"></a>Функция Стандардамплитудеамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL

Операция, реализующая стандартный алгоритм такта для усиления амплитуды

## <a name="remarks"></a>Комментарии

Это стандартный алгоритм усиления амплитуды, полученный при выборе фаз отражения, вычисленных при `AmpAmpPhasesStandard` условии, что \Бегин{алигн} а\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} эта операция готовит состояние \бегин{алигн} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ Text {Target}} \_ s + \cdots\ket {0} \_ f \end{align} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируется в состоянии $ \ket {0} \_ f\ket {0} \_ a $.

## <a name="references"></a>Ссылки

- [*G. Брассард, P. Хойер, M. Моска, A. касание*](https://arxiv.org/abs/quant-ph/0005055)