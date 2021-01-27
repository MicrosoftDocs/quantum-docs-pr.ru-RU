---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Операция Апплитофирсттвокубитск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f71209a806b0d1d712a3c776eb45e62d1cd5d5f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841353"
---
# <a name="applytofirsttwoqubitsc-operation"></a>Операция Апплитофирсттвокубитск

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым двум Кубитс в регистре.
Модификатор `C` указывает, что операция является управляемой.

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit--is-ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) => [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

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