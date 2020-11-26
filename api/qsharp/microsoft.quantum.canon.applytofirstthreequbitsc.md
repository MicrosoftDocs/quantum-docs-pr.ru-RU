---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: Операция Апплитофирстсрикубитск
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: cb6945f5aa398d0bf6417c5cfd21142008a54b13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217447"
---
# <a name="applytofirstthreequbitsc-operation"></a>Операция Апплитофирстсрикубитск

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым трем Кубитс в регистре.
Модификатор `C` указывает, что операция является управляемой.

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubitqubit--unit--is-ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [модуль](xref:microsoft.quantum.lang-ref.unit) > является CTL

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