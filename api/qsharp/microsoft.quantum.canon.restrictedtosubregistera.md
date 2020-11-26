---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: Функция Рестриктедтосубрегистера
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 28128641a95c6948b5fa5730bf3bd90aa6bb1ef5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205292"
---
# <a name="restrictedtosubregistera-function"></a>Функция Рестриктедтосубрегистера

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ограничивают операцию массивом индексов регистра, т. е. подрегистром.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, которая должна быть ограничена подрегистром.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому Кубитс операция будет ограничена.



## <a name="output--qubit--unit--is-adj"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рестриктедтосубрегистер](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)