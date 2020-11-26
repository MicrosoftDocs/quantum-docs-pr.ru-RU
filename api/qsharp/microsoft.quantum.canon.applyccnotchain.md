---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Операция Аппликкнотчаин
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 275f31ea636d15eb0d78e5148e8af6b58d22729d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209661"
---
# <a name="applyccnotchain-operation"></a>Операция Аппликкнотчаин

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует каскадный шлюз ККНОТ, управляемый по соответствующим битам двух регистров кубит, который действует на следующий кубит одного из регистров.
Начиная с Кубитс в позиции 0 в обоих регистрах как элементы управления, ККНОТ применяется к кубит в позиции 1 целевого регистра, затем управляется Кубитс в позиции 1, действующей на кубит в позиции 2 в целевой регистрации, и т. д., заканчивая действием на целевом кубит в позиции `Length(nQubits)-1` .

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит регистр, используемый только для элементов управления.


### <a name="targets--qubit"></a>целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, используемый для элементов управления и в качестве целевого объекта.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Целевой регистр кубит должен иметь один кубит больше, чем другой регистр.