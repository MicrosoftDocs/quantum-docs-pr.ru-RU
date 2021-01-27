---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Функция Обливиаусамплитудеамплификатионфромстатепрепаратион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 873c436d4b8d8efc9dc61c2baba9b0e0f7f09fc2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845822"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>Функция Обливиаусамплитудеамплификатионфромстатепрепаратион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Усиление амплитуды очевидным по Oracle для частичных отражений.

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="phases--reflectionphases"></a>этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Фазы частичной отражения


### <a name="startstateoracle--deterministicstateoracle"></a>Стартстатеоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Единая база данных Oracle $A $, подготавливающая дополнительное состояние запуска


### <a name="signaloracle--obliviousoracle"></a>Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Единая база данных Oracle $O $ типа `ObliviousOracle` , которая взаимодействует с дополнительным и системным регистром


### <a name="idxflagqubit--int"></a>Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)

Регистр индекса для однокубитного флага



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, реализующая усиление амплитуды очевидным на основе частичных отражений.

## <a name="remarks"></a>Remarks

Это накладывает более четкие условия на формат начального и целевого состояний, чем в `AmpAmpObliviousByReflectionPhases` .
Предполагается, что $A \кет {0} \_ ф\кет {0} \_ A = \кет{\текст{старт}} \_ {FA} $ подготавливает вспомогательное состояние запуска $ \кет{\текст{старт}} \_ {FA} $ от вычислительной базы $ \кет {0} \_ ф\кет {0} $.
Предполагается, что целевое состояние помечено как $ \кет {1} \_ f $.
Предполагается, что \бегин{алигн} О\кет {\ Text {Start}} \_ {FA} \кет{\пси} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {ничего}} \_ а\кет {\ Text {Target}} \_ s U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \end{align} для некоторых $U $.