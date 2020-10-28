---
uid: Microsoft.Quantum.Core.Deprecated
title: Нерекомендуемый определяемый пользователем тип
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: b1fcae9647b2a655d25773386ecffa826515516e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713270"
---
# <a name="deprecated-user-defined-type"></a>Нерекомендуемый определяемый пользователем тип

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакеты [](https://nuget.org/packages/)


Распознанный компилятором атрибут, используемый для пометки типа или вызываемого как нерекомендуемый.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Именованные элементы

### <a name="newname--string"></a>NewName: [строка](xref:microsoft.quantum.lang-ref.string)

Полное имя типа или вызываемого для использования.
Параметру присваивается пустая строка, если тип или вызываемый объект не рекомендуется использовать без подстановки.