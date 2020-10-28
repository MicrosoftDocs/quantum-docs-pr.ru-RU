---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Функция Контролледонинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716419"
---
# <a name="controlledonint-function"></a>Функция Контролледонинт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Возвращает оператор, который применяет объект Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданному положительному целому числу.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="numberstate--int"></a>Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)

Положительное целое число.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Оператор с единым.



## <a name="output--qubitt--unit-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) = [>ная](xref:microsoft.quantum.lang-ref.unit) Расгода и список доверия

Оператор, применяемый к `oracle` целевому регистру, если состояние регистра элемента управления соответствует состоянию числа `numberState` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.