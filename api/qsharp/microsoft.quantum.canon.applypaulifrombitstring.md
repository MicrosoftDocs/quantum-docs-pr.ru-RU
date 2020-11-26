---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Операция Апплипаулифромбитстринг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209066"
---
# <a name="applypaulifrombitstring-operation"></a>Операция Апплипаулифромбитстринг

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет оператор Паули к каждому кубит в массиве, если соответствующий бит логического массива совпадает с заданным входным значением.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор Паули для применения к `qubits[idx]` месту `bitsApply == bits[idx]`


### <a name="bitapply--bool"></a>Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)

применить Паули, если бит — это значение


### <a name="bits--bool"></a>Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Логический регистр, указывающий, на какие соответствующие кубит `qubits` должны работать


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, на котором выборочно применяется указанный оператор Паули



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Логический массив и регистр такта должны иметь одинаковую длину.