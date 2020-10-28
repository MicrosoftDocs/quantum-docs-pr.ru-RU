---
uid: Microsoft.Quantum.Logical.Conditioned
title: Условная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731296"
---
# <a name="conditioned-function"></a>Условная функция

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакеты [](https://nuget.org/packages/)


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

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```