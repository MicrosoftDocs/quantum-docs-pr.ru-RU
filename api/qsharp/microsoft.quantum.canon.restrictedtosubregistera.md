---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: Функция Рестриктедтосубрегистера
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: d45c43caed35df8fb89d9d38e540faf5a21ea064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715537"
---
# <a name="restrictedtosubregistera-function"></a>Функция Рестриктедтосубрегистера

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Ограничивают операцию массивом индексов регистра, т. е. подрегистром.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция, которая должна быть ограничена подрегистром.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому Кубитс операция будет ограничена.



## <a name="output--qubit--unit-adj"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рестриктедтосубрегистер](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)