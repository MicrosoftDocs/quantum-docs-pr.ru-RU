---
uid: Microsoft.Quantum.Canon.CControlledCA
title: Функция Кконтролледка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 20a8c9ccf931261f7bc6e347ccc144c92f0d0545
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716573"
---
# <a name="ccontrolledca-function"></a>Функция Кконтролледка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true. Если `false` значение равно, ничего не происходит.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl--adj"></a>Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Операция, применяемая к условию.



## <a name="output--boolt--unit-ctl--adj"></a>Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Новая операция, выполняемая, если классический контрольный бит имеет значение true.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кконтроллед](xref:Microsoft.Quantum.Canon.CControlled)