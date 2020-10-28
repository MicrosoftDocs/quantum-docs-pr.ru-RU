---
uid: Microsoft.Quantum.Canon.OperationPow
title: Функция Оператионпов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715775"
---
# <a name="operationpow-function"></a>Функция Оператионпов

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Порождает операцию в степень.

То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция $U $, представляющая шлюз, который должен повторяться.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Количество повторных попыток $U $.



## <a name="output--t--unit"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit) 

Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип операции, которая должна быть включена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Оператионповк](xref:Microsoft.Quantum.Canon.OperationPowC)
- [Microsoft. тактов. Canon. Оператионпова](xref:Microsoft.Quantum.Canon.OperationPowA)
- [Microsoft. тактов. Canon. Оператионповка](xref:Microsoft.Quantum.Canon.OperationPowCA)