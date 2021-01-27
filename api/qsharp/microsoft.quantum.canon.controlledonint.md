---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Функция Контролледонинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840784"
---
# <a name="controlledonint-function"></a>Функция Контролледонинт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает оператор, который применяет объект Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданному положительному целому числу.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="numberstate--int"></a>Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)

Положительное целое число.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Оператор с единым.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Оператор, применяемый к `oracle` целевому регистру, если состояние регистра элемента управления соответствует состоянию числа `numberState` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.