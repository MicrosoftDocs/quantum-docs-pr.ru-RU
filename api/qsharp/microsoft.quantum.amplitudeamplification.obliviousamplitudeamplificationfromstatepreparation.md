---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Функция Обливиаусамплитудеамплификатионфромстатепрепаратион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731977"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>Функция Обливиаусамплитудеамплификатионфромстатепрепаратион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


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



## <a name="output--qubitqubit--unit-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия

Операция, реализующая усиление амплитуды очевидным на основе частичных отражений.

## <a name="remarks"></a>Remarks

Это накладывает более четкие условия на формат начального и целевого состояний, чем в `AmpAmpObliviousByReflectionPhases` .
Предполагается, что $A \кет {0} \_ ф\кет {0} \_ A = \кет{\текст{старт}} \_ {FA} $ подготавливает вспомогательное состояние запуска $ \кет{\текст{старт}} \_ {FA} $ от вычислительной базы $ \кет {0} \_ ф\кет {0} $.
Предполагается, что целевое состояние помечено как $ \кет {1} \_ f $.
Предполагается, что \бегин{алигн} О\кет {\ Text {Start}} \_ {FA} \кет{\пси} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {ничего}} \_ а\кет {\ Text {Target}} \_ s U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \end{align} для некоторых $U $.