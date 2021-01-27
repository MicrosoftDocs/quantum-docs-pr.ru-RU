---
uid: Microsoft.Quantum.Logical.Conditioned
title: Условная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817288"
---
# <a name="conditioned-function"></a>Условная функция

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает одно из двух значений в зависимости от значения логического условия.

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a>Входные данные

### <a name="condition--bool"></a>условие: [логическое](xref:microsoft.quantum.lang-ref.bool) значение

Условие, используемое для управления возвращаемыми входными данными.


### <a name="iftrue--t"></a>ifTrue: 'T

Значение, возвращаемое, если `condition` равно `true` .


### <a name="iffalse--t"></a>ifFalse: 'T

Значение, возвращаемое, если `condition` равно `false` .



## <a name="output--t"></a>Выходные данные: 'T

`ifTrue` Если `condition` имеет значение `true` , и `ifFalse` в противном случае —.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

В отличие от `?|` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.

Ниже приведены эквивалентные действия для сокращенного поведения.

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```