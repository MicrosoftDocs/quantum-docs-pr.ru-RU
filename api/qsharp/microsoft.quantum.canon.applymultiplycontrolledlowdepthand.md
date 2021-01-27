---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Операция Апплимултипликонтролледловдепсанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 0ad4b6eabcbbb63751489dd92a13a6673c1ae6b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841675"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a>Операция Апплимултипликонтролледловдепсанд

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.  При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.  Требуется РЗ глубина 1, а число вспомогательных Кубитс — экспоненциальное число Кубитс.

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="controls--qubit"></a>элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Управление Кубитс


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

