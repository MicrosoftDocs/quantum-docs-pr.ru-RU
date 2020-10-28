---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Функция Оператионповка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715677"
---
# <a name="operationpowca-function"></a>Функция Оператионповка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Порождает операцию в степень.
Модификатор `A` указывает, что операция является управляемой и аджоинтабле.

То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl--adj"></a>Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Операция $U $, представляющая шлюз, который должен повторяться.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Количество повторных попыток $U $.



## <a name="output--t--unit-ctl--adj"></a>Выходные данные: 'T => [единицу](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип операции, которая должна быть включена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Оператионпов](xref:Microsoft.Quantum.Canon.OperationPow)