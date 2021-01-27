---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Функция Оператионповка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 338c40f8eb9d6f1782989f2a91c86df561d480bf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852308"
---
# <a name="operationpowca-function"></a>Функция Оператионповка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Порождает операцию в степень.
Модификатор `A` указывает, что операция является управляемой и аджоинтабле.

То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-adj--ctl"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция $U $, представляющая шлюз, который должен повторяться.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Количество повторных попыток $U $.



## <a name="output--t--unit--is-adj--ctl"></a>Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL

Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип операции, которая должна быть включена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Оператионпов](xref:Microsoft.Quantum.Canon.OperationPow)