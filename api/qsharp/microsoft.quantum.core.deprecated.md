---
uid: Microsoft.Quantum.Core.Deprecated
title: Нерекомендуемый определяемый пользователем тип
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 122cbc113a68cec107558d68a6fb145cf6bbd9db
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224094"
---
# <a name="deprecated-user-defined-type"></a>Нерекомендуемый определяемый пользователем тип

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Распознанный компилятором атрибут, используемый для пометки типа или вызываемого как нерекомендуемый.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Именованные элементы

### <a name="newname--string"></a>NewName: [строка](xref:microsoft.quantum.lang-ref.string)

Полное имя типа или вызываемого для использования.
Параметру присваивается пустая строка, если тип или вызываемый объект не рекомендуется использовать без подстановки.