---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Операция Апплитосубрегистера
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7a5ae78edcda363f21cadaaed5cb273d35cb60cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841226"
---
# <a name="applytosubregistera-operation"></a>Операция Апплитосубрегистера

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к подрегистру регистра с Кубитс, заданным массивом своих индексов.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, применяемая к подрегистру.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому кубитсу будет применена операция.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация, в которой действует операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитосубрегистер](xref:Microsoft.Quantum.Canon.ApplyToSubregister)