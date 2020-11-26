---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA
title: Операция Апплитофирсттвокубитска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsCA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: a2281776b617d5c3f8cc706ea09d14995fce4a27
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208658"
---
# <a name="applytofirsttwoqubitsca-operation"></a>Операция Апплитофирсттвокубитска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым двум Кубитс в регистре.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
operation ApplyToFirstTwoQubitsCA (op : ((Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit--is-adj--ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, применяемая к первым двум Кубитс


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первым двум Кубитс, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Это соответствует следующей записи:

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирсттвокубитс](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)