---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Операция Апплямплитудеамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: 8fd5c3f20c5a5aaae140feaf3af02395bff77b9c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845884"
---
# <a name="applyamplitudeamplification-operation"></a>Операция Апплямплитудеамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет усиление амплитуды к заданному регистру, используя заданный набор фаз и Oracle, чтобы отражать начальное и конечное состояния.

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="phases--reflectionphases"></a>этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Набор этапов, описывающих частичные отражения на каждом шаге алгоритма усиления амплитуды. Пример см. в разделе @"microsoft.quantum.amplitudeamplification.standardreflectionphases".


### <a name="startstatereflection--reflectionoracle"></a>Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Oracle, отражающий начальное состояние.


### <a name="targetstatereflection--reflectionoracle"></a>Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Значение Oracle, отражающее требуемое конечное состояние.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр для выполнения усиления амплитуды.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

