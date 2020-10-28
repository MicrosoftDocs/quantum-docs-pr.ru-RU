---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Определяемый пользователем тип Рекуирескапабилити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 63b1952d402f1bcb81a8f9d0afc3cdf7aa7e5ed8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733865"
---
# <a name="requirescapability-user-defined-type"></a>Определяемый пользователем тип Рекуирескапабилити

Пространство имен: [Microsoft. тактов. нацеливание](xref:Microsoft.Quantum.Targeting)

Пакеты [](https://nuget.org/packages/)


Распознанный компилятором атрибут, используемый для пометки вызываемого с возможностями среды выполнения, которые он требует.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a>Именованные элементы

### <a name="level--string"></a>Level: [строка](xref:microsoft.quantum.lang-ref.string)

Имя уровня возможностей среды выполнения, требуемого для вызываемого объекта.
### <a name="reason--string"></a>Причина: [строка](xref:microsoft.quantum.lang-ref.string)

Описание причин, по которым вызываемый объект требует этой возможности среды выполнения.

## <a name="remarks"></a>Remarks

Этот атрибут автоматически добавляется в вызываемые компилятором, если в вызываемом экземпляре уже не существует экземпляра этого атрибута. Его не следует использовать, за исключением редких случаев, когда компилятор неправильно выводит требуемую возможность.

Ниже приведен список имен уровней возможностей в порядке увеличения возможностей или снижения ограничений.

## `"BasicQuantumFunctionality"`

Результаты измерения не могут сравниваться на равенство.

## `"BasicMeasurementFeedback"`

Результаты измерения можно сравнивать на равенство только в условных выражениях if-операторах в операциях. Блок оператора if, который зависит от результата, не может содержать инструкции SET для изменяемых переменных, объявленных за пределами блока, или операторов return.

## `"FullComputation"`

Нет ограничений среды выполнения. Можно выполнить любую программу Q #.