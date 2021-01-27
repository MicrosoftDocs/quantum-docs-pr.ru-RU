---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Определяемый пользователем тип Рекуирескапабилити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 5e0db49d6f73398ac36003eb0f44e3a6520b7f1e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855158"
---
# <a name="requirescapability-user-defined-type"></a>Определяемый пользователем тип Рекуирескапабилити

Пространство имен: [Microsoft. тактов. нацеливание](xref:Microsoft.Quantum.Targeting)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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