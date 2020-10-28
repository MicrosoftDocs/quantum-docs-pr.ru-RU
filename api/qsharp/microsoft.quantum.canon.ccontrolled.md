---
uid: Microsoft.Quantum.Canon.CControlled
title: Функция Кконтроллед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716588"
---
# <a name="ccontrolled-function"></a>Функция Кконтроллед

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии операции операция возвращает новую операцию, которая применяет оператор, если классический контрольный бит имеет значение true. Если `false` значение равно, ничего не происходит.

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, применяемая к условию.



## <a name="output--boolt--unit"></a>Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Новая операция, выполняемая, если классический контрольный бит имеет значение true.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Кконтролледк](xref:Microsoft.Quantum.Canon.CControlledC)
- [Microsoft. тактов. Canon. Кконтролледа](xref:Microsoft.Quantum.Canon.CControlledA)
- [Microsoft. тактов. Canon. Кконтролледка](xref:Microsoft.Quantum.Canon.CControlledCA)