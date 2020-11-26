---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Функция Рестриктедтосубрегистерк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e03f695ea5943bc2296b0ef1ce613f7835a87c5a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205258"
---
# <a name="restrictedtosubregisterc-function"></a>Функция Рестриктедтосубрегистерк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ограничивают операцию массивом индексов регистра, т. е. подрегистром.
Модификатор `C` указывает, что операция является управляемой.

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-ctl"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL

Операция, которая должна быть ограничена подрегистром.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому Кубитс операция будет ограничена.



## <a name="output--qubit--unit--is-ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  CTL



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рестриктедтосубрегистер](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)