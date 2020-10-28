---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Операция Апплитосубрегистерка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 3eb210debf8980f057ed150f647d545f68734459
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716993"
---
# <a name="applytosubregisterca-operation"></a>Операция Апплитосубрегистерка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit-ctl--adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]> = [единица](xref:microsoft.quantum.lang-ref.unit) CTL + года

Операция, применяемая к подрегистру.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому кубитсу будет применена операция.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация, в которой действует операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитосубрегистер](xref:Microsoft.Quantum.Canon.ApplyToSubregister)