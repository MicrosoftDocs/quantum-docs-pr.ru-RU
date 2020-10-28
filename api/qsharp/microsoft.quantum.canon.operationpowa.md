---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Функция Оператионпова
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 66df354c6de7e48624712276882759043b78466c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715719"
---
# <a name="operationpowa-function"></a>Функция Оператионпова

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Порождает операцию в степень.
Модификатор `A` указывает, что операция является аджоинтабле.

То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj"></a>Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Операция $U $, представляющая шлюз, который должен повторяться.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Количество повторных попыток $U $.



## <a name="output--t--unit-adj"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit) прогода

Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип операции, которая должна быть включена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Оператионпов](xref:Microsoft.Quantum.Canon.OperationPow)