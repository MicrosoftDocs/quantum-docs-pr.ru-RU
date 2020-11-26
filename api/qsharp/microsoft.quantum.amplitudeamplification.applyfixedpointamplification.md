---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191539"
---
# <a name="applyfixedpointamplification-operation"></a>Операция Апплификседпоинтамплификатион

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Комментарии

Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $. Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.