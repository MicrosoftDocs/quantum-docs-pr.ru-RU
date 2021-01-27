---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: Функция Рестриктедтосубрегистер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: c5a6bbe16d2f6a317f6ed6f258077095465995f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840230"
---
# <a name="restrictedtosubregister-function"></a>Функция Рестриктедтосубрегистер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ограничивают операцию массивом индексов регистра, т. е. подрегистром.

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которая должна быть ограничена подрегистром.


### <a name="idxs--int"></a>идксс: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, указывающий, к какому Кубитс операция будет ограничена.



## <a name="output--qubit--unit"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Рестриктедтосубрегистера](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [Microsoft. тактов. Canon. Рестриктедтосубрегистерк](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [Microsoft. тактов. Canon. Рестриктедтосубрегистерка](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)