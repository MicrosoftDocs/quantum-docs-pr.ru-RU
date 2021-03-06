---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Операция Апплиловдепсанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 7fa9d9bf2f1905bf1b59e783d7bceb8cb2e09fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841703"
---
# <a name="applylowdepthand-operation"></a>Операция Апплиловдепсанд

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Инвертирует заданный целевой объект кубит только в том случае, если оба элемента управления Кубитс находятся в состоянии 1 с T-Depth 1, с помощью измерения для выполнения примыкающей операции.

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Инвертирует `target` , если оба элемента управления равны 1, но предполагает, что `target` находится в состоянии 0.  Операция имеет T-Count 4, T-Depth 1 и требует одного вспомогательного кубит и, следовательно, может быть предпочтительнее операции ККНОТ, если `target` известно как 0.  Смежная часть этой операции основана на измерении и не требует T-шлюзов и не имеет вспомогательного кубит.

## <a name="input"></a>Входные данные

### <a name="control1--qubit"></a>Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый элемент управления кубит


### <a name="control2--qubit"></a>control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй элемент управления кубит


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой вспомогательный кубит; должно находиться в состоянии 0



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Коди Jones: "романские конструкции для отказоустойчивого Тоффоли шлюза", инвентаризационная. Rev. A 87, 022328, 2013 [арксив: 1212.5069](https://arxiv.org/abs/1212.5069) ДОИ: 10.1103/фисрева. 87.022328
- Питер Селинжер: "тактовые цепи T-Depth 1", инвентаризационная. Rev. A 87, 042302, 2013 [арксив: 1210.0974](https://arxiv.org/abs/1210.0974) ДОИ: 10.1103/фисрева. 87.042302