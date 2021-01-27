---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Операция Аппликонтролледонинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 499a25104742b2d03886065baad4d535ea92e83b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845102"
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



## <a name="remarks"></a>Remarks

Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.

`numberState` должно быть не более $2 ^ \Тексттт{ленгс (Контролрегистер)}-$1.
Например, это `numberState = 537` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {537} $.