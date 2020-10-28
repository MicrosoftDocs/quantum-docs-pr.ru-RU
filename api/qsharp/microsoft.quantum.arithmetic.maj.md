---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Операция Shift
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731448"
---
# <a name="maj-operation"></a>Операция Shift

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Это применяет операцию большинства "на месте" к 3 Кубитс.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
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

