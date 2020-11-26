---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Операция Shift
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 356689baa6d47b7b93a393f3672991bb589f6921
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222768"
---
# <a name="maj-operation"></a>Операция Shift

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Это применяет операцию большинства "на месте" к 3 Кубитс.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Если мы обкубит состояние целевого объекта как $ \кет{з} $, а входные состояния входных Кубитс как $ \кет{КС} $ и $ \кет{и} $, эта операция выполняет следующее преобразование: $ \кет{ксиз} \ригхтарров \кет{КС \оплус z} \кет{и \оплус z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>Входные данные

### <a name="input0--qubit"></a>input0: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый входной кубит.


### <a name="input1--qubit"></a>INPUT1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй входной кубит.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, на который будет применена функция большинства.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

