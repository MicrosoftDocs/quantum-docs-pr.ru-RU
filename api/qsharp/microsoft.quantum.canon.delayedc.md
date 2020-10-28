---
uid: Microsoft.Quantum.Canon.DelayedC
title: Функция Делайедк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716210"
---
# <a name="delayedc-function"></a>Функция Делайедк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Возвращает операцию, которая применяет заданную операцию с заданным аргументом.

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl"></a>Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL

Операция, применяемая в результате применения возвращаемого значения


### <a name="arg--t"></a>ARG: 'T

Входные данные, к которым `op` применяется операция.



## <a name="output--unit--unit-ctl"></a>Выходные данные [Unit](xref:microsoft.quantum.lang-ref.unit) : => список доверия [единиц](xref:microsoft.quantum.lang-ref.unit) измерения

Новая операция, которая применяется `op` с входными данными `arg`

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Входной тип операции, которая должна быть отложена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. DELAYED](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. тактов. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)