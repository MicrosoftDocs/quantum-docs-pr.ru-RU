---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Операция Аппликонтролледонинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: c8ea76946143967de4b6ac65986a1c4407ecb633
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729672"
---
# <a name="applycontrolledonint-operation"></a>Операция Аппликонтролледонинт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет единую операцию к целевой регистрации, если контрольное состояние реестра соответствует заданному положительному целому числу.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a>Входные данные

### <a name="numberstate--int"></a>Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)

Неотрицательное целое число, на которое `oracle` должна контролироваться операция.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Единая операция для управления.


### <a name="controlregister--qubit"></a>Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, который управляет приложением `oracle` .


### <a name="targetregister--t"></a>Таржетрегистер: 'T

Регистр, к которому применяется `oracle` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.

`numberState` должно быть не более $2 ^ \Тексттт{ленгс (Контролрегистер)}-$1.
Например, это `numberState = 537` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {537} $.