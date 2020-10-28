---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Операция Апплитофирсткубита
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 00dbff0b562f90653c8569589e838f11e6c938e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717400"
---
# <a name="applytofirstqubita-operation"></a>Операция Апплитофирсткубита

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию к первому кубиту в регистре.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)

Операция, применяемая к первому кубит


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первому кубит, к которому применяется операция



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирсткубит](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)