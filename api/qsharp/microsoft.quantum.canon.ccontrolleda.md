---
uid: Microsoft.Quantum.Canon.CControlledA
title: Функция Кконтролледа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 823d80182621691f4fa6f42246b3d671f3adfc3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840994"
---
# <a name="ccontrolleda-function"></a>Функция Кконтролледа

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true. Если `false` значение равно, ничего не происходит.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-adj"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой

Операция, применяемая к условию.



## <a name="output--boolt--unit--is-adj"></a>Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)

Новая операция, выполняемая, если классический контрольный бит имеет значение true.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кконтроллед](xref:Microsoft.Quantum.Canon.CControlled)