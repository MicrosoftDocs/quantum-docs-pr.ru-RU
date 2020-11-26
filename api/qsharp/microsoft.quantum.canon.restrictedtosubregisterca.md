---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Функция Рестриктедтосубрегистерка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: e45206f5e829b7d30f9782e9e5b4c85ae52a1ea6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205309"
---
# <a name="restrictedtosubregisterca-function"></a>Функция Рестриктедтосубрегистерка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ограничивают операцию массивом индексов регистра, т. е. подрегистром.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-adj--ctl"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которая должна быть ограничена подрегистром.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому Кубитс операция будет ограничена.



## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рестриктедтосубрегистер](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)