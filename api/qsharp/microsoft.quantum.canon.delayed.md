---
uid: Microsoft.Quantum.Canon.Delayed
title: Отложенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716252"
---
# <a name="delayed-function"></a>Отложенная функция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Возвращает операцию, которая применяет заданную операцию с заданным аргументом.

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a>Входные данные

### <a name="op--t--u"></a>Op: 'T => ' U 

Операция, которую необходимо применить.


### <a name="arg--t"></a>ARG: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit--u"></a>Выходные данные: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U 

Новая операция, которая применяется `op` с входными данными `arg`

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Входной тип операции, которая должна быть отложена.
### <a name="u"></a>' U

Возвращаемый тип операции, которая должна быть отложена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Делайедк](xref:Microsoft.Quantum.Canon.DelayedC)
- [Microsoft. тактов. Canon. DELAYED](xref:Microsoft.Quantum.Canon.DelayedA)
- [Microsoft. тактов. Canon. Делайедка](xref:Microsoft.Quantum.Canon.DelayedCA)
- [Microsoft. тактов. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)