---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: Операция Апплитофирстсрикубитса
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c3374ceba9f442f9315d4b5fc54b158327124926
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208777"
---
# <a name="applytofirstthreequbitsa-operation"></a>Операция Апплитофирстсрикубитса

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым трем Кубитс в регистре.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubitqubit--unit--is-adj"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) => [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме

Операция, применяемая к первым трем Кубитс


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первым трем Кубитс, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Это соответствует следующей записи:

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирстсрикубитс](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)