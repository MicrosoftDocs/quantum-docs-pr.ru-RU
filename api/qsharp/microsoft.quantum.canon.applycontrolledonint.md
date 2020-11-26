---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Операция Аппликонтролледонинт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3dd17e6bc913e84941a6b81f134e60536a4c4122
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219011"
---
# <a name="applycontrolledonint-operation"></a>Операция Аппликонтролледонинт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет единую операцию к целевой регистрации, если контрольное состояние реестра соответствует заданному положительному целому числу.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="numberstate--int"></a>Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)

Неотрицательное целое число, на которое `oracle` должна контролироваться операция.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Единая операция для управления.


### <a name="controlregister--qubit"></a>Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, который управляет приложением `oracle` .


### <a name="targetregister--t"></a>Таржетрегистер: 'T

Регистр, к которому применяется `oracle` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Комментарии

Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.

`numberState` должно быть не более $2 ^ \Тексттт{ленгс (Контролрегистер)}-$1.
Например, это `numberState = 537` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {537} $.