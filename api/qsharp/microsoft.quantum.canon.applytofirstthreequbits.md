---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Операция Апплитофирстсрикубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: b01c1072306cfdebcb90827a14683a32312481fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850704"
---
# <a name="applytofirstthreequbits-operation"></a>Операция Апплитофирстсрикубитс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым трем Кубитс в регистре.

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubitqubit--unit"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

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

- [Microsoft. тактов. Canon. Апплитофирстсрикубитск](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [Microsoft. тактов. Canon. Апплитофирстсрикубитса](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [Microsoft. тактов. Canon. Апплитофирстсрикубитска](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)