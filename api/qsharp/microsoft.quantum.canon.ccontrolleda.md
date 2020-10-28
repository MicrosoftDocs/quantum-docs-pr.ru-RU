---
uid: Microsoft.Quantum.Canon.CControlledA
title: Функция Кконтролледа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 30b5e3408fa6e5a79b2f3d63cccc11899c0405ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716587"
---
# <a name="ccontrolleda-function"></a>Функция Кконтролледа

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true. Если `false` значение равно, ничего не происходит.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj"></a>Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Операция, применяемая к условию.



## <a name="output--boolt--unit-adj"></a>Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Новая операция, выполняемая, если классический контрольный бит имеет значение true.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кконтроллед](xref:Microsoft.Quantum.Canon.CControlled)