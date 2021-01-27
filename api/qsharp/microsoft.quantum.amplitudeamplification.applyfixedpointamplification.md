---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: fa19c3bb06ae91a2fa18acb6f853020830e749f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847234"
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



## <a name="remarks"></a>Remarks

Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $. Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.