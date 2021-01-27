---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA
title: Операция Апплитофирстсрикубитска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsCA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9bc5248b5de0db60f54bbec4cb33dde1160c2b41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841378"
---
# <a name="applytofirstthreequbitsca-operation"></a>Операция Апплитофирстсрикубитска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым трем Кубитс в регистре.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
operation ApplyToFirstThreeQubitsCA (op : ((Qubit, Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubitqubit--unit--is-adj--ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, применяемая к первым трем Кубитс


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первым трем Кубитс, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Это соответствует следующей записи:

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирстсрикубитс](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)