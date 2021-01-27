---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Операция Апплифермиониксвап
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 334f407a32dabc8f4e0a1a29c8f06a1b9f40dc59
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845050"
---
# <a name="applyfermionicswap-operation"></a>Операция Апплифермиониксвап

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет ПЕРЕМЕНную Фермионик.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Это по сути меняет местами Кубитс при применении глобального этапа – 1, если оба Кубитс равны 1. Сохраняет симметризатион орбиты.
Дополнительные сведения см. в разделе .

Эта операция представлена единым оператором \бегин{алигн} f_ {swap} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \енд{бматрикс}.
\енд{алигн}

## <a name="input"></a>Входные данные

### <a name="qubit1--qubit"></a>qubit1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый кубит, который необходимо поменять местами.


### <a name="qubit2--qubit"></a>qubit2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй кубит, который необходимо поменять местами.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- [*Райан баббуш, (Nathan виебе, Жаррод Астрид, Джеймс мкклаин, Хартмут Невен, гарнет Kin-Lic* канал, арксив: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. внутренний. SWAP](xref:Microsoft.Quantum.Intrinsic.SWAP)