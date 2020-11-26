---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Операция Аппликнотчаинвистаржет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: 8ec85ce5805b3bbd1e1f7c739f27de3a861bc79e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219113"
---
# <a name="applycnotchainwithtarget-operation"></a>Операция Аппликнотчаинвистаржет

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет подсчет четности массива Кубитс в целевом кубит.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Если изначально массив находится в состоянии $ \кет{q_0} \кет{q_1} \кдотс \кет{q_ {\текст{таржет}}} $, конечное состояние присваивается с помощью $ \кет{q_0} \кет{q_1 \оплус q_0} \кдотс \кет{q_ {n-1} \оплус \кдотс \oplus q_0 \oplus q_ {\Text{Target}}} $.

## <a name="input"></a>Входные данные

### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив Кубитс, для которого вычислена четность.


### <a name="targetqubit--qubit"></a>Таржеткубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Окончательный кубит, в котором четностью Кубитс является Ксоред.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

и

```qsharp
ApplyCNOTChain(qs);
```