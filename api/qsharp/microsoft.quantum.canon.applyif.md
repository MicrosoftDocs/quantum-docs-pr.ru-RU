---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Операция Апплиф
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c8f6860a7a3b8af86b0edb048baccbf057dd245a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729600"
---
# <a name="applyif-operation"></a>Операция Апплиф

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию с условием на Классический бит.

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` . Если значение `false` равно, то ничего не происходит с `target` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, применяемая к условию.


### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, определяющее, применяется ли оператор Op.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифк](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. тактов. Canon. Апплифа](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft. тактов. Canon. Апплифка](xref:Microsoft.Quantum.Canon.ApplyIfCA)