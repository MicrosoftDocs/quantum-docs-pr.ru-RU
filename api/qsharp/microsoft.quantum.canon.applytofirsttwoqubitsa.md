---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Операция Апплитофирсттвокубитса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 197f1da6682b100a0b71f3548727188c0ef6f7c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850674"
---
# <a name="applytofirsttwoqubitsa-operation"></a>Операция Апплитофирсттвокубитса

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым двум Кубитс в регистре.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit--is-adj"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) => [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме

Операция, применяемая к первым двум Кубитс


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первым двум Кубитс, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Это соответствует следующей записи:

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирсттвокубитс](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)