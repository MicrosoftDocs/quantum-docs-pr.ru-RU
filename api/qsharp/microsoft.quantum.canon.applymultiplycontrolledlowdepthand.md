---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Операция Апплимултипликонтролледловдепсанд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 6900f9b0f014fba28ae73a70f180f3e4696900cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717946"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a>Операция Апплимултипликонтролледловдепсанд

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.  При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.  Требуется РЗ глубина 1, а число вспомогательных Кубитс — экспоненциальное число Кубитс.

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="controls--qubit"></a>элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Управление Кубитс


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

