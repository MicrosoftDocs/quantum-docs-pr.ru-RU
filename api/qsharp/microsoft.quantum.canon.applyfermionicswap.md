---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Операция Апплифермиониксвап
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 25dd91b200700d1474cf27bf1d0fa71d57f2e09b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729617"
---
# <a name="applyfermionicswap-operation"></a>Операция Апплифермиониксвап

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет ПЕРЕМЕНную Фермионик.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
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