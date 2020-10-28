---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732024"
---
# <a name="applyfixedpointamplification-operation"></a>Операция Апплификседпоинтамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Fixed-Point алгоритм усиления амплитуды

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="statepreporacle--stateoracle"></a>Статепрепоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)

Единая база данных Oracle, подготавливающая начальное состояние.


### <a name="startqubits--qubit"></a>Старткубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит регистр



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $. Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.