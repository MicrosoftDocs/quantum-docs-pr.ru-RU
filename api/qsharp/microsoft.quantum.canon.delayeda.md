---
uid: Microsoft.Quantum.Canon.DelayedA
title: Отложенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716251"
---
# <a name="delayeda-function"></a>Отложенная функция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Возвращает операцию, которая применяет заданную операцию с заданным аргументом.

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj"></a>Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Операция, применяемая в результате применения возвращаемого значения


### <a name="arg--t"></a>ARG: 'T

Входные данные, к которым `op` применяется операция.



## <a name="output--unit--unit-adj"></a>Выходные данные: поправка единицы [единицы измерения](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)

Новая операция, которая применяется `op` с входными данными `arg`

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Входной тип операции, которая должна быть отложена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. DELAYED](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. тактов. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)