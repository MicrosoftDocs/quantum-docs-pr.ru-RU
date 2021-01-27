---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Операция Апплйобливиаусамплитудеамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: c171021272076cc3960307523e25c4493bb49c5a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845876"
---
# <a name="applyobliviousamplitudeamplification-operation"></a>Операция Апплйобливиаусамплитудеамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Усиление амплитуды очевидным путем указания частичных отражений.

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="phases--reflectionphases"></a>этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Фазы частичной отражения


### <a name="startstatereflection--reflectionoracle"></a>Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Оператор Reflection о начальном состоянии дополнительного регистра


### <a name="targetstatereflection--reflectionoracle"></a>Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Оператор отражения о целевом состоянии дополнительного регистра


### <a name="signaloracle--obliviousoracle"></a>Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Единая база данных Oracle $O $ типа `ObliviousOracle` , которая взаимодействует с вспомогательными и системными регистрами.


### <a name="auxiliaryregister--qubit"></a>Ауксилиарирегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Дополнительный регистр


### <a name="systemregister--qubit"></a>Системрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Системный регистр



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Учитывая определенное вспомогательное состояние запуска $ \кет{\текст{старт}} \_ $, определенное вспомогательное состояние $ \кет{\текст{таржет}} \_ a $ и любое состояние системы $ \кет{\пси} \_ s $, предположим, что \бегин{алигн} о\кет {\ Text {Start}} \_ а\кет {\ PSI} \_ s = \ламбда\кет{\текст{таржет}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\Text{Target} ^ \perp} \_ a\cdots \end{align} для $U $.
По последовательности отражений состояний запуска и целевого объекта вспомогательной ККМ, которая загружается приложениями `signalOracle` и соседними, вероятность успешного применения U может быть изменена.

В большинстве случаев `auxiliaryRegister` инициализируется в состоянии $ \кет{\текст{старт}} \_ a $.

## <a name="references"></a>Ссылки

См.

- [ *Д.в. Берри, дочерние, r. Cleve, r. Котари, р.д. Сомма*](https://arxiv.org/abs/1312.1414) для стандартной версии.
  См.
- [ *Г.х. Low, и.л. Чжуанский*](https://arxiv.org/abs/1610.06546) для обобщения с частичными отражениями.