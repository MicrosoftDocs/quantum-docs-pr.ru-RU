---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Операция Апплитофирсттвокубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: c89ea89c055a950a9aee533653d40c84d8e179da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841366"
---
# <a name="applytofirsttwoqubits-operation"></a>Операция Апплитофирсттвокубитс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первым двум Кубитс в регистре.

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

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

- [Microsoft. тактов. Canon. Апплитофирсттвокубитса](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [Microsoft. тактов. Canon. Апплитофирсттвокубитск](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [Microsoft. тактов. Canon. Апплитофирсттвокубитска](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)