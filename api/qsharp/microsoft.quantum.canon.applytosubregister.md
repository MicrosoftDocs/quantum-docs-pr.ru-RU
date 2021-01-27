---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Операция Апплитосубрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: be820c87ee19230713d6c3e5681bbe3678040e95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850467"
---
# <a name="applytosubregister-operation"></a>Операция Апплитосубрегистер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, применяемая к подрегистру.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому кубитсу будет применена операция.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация, в которой действует операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

Создайте три состояния кубит $ \фрак {1} {\скрт {2} } \кет {0} \_ 2 (\кет {0} \_ 1 \ Сисакет {0} _3 + \кет {1} \_ 1 \ Сисакет {1} _3) $:

```qsharp
    using (register = Qubit[3]) {
        ApplyToSubregister(Exp([PauliX,PauliY],PI() / 4.0,_), [1,3], register);
    }
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитосубрегистера](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [Microsoft. тактов. Canon. Апплитосубрегистерк](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [Microsoft. тактов. Canon. Апплитосубрегистерка](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)