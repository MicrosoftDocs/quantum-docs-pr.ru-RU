---
uid: Microsoft.Quantum.Core.Deprecated
title: Нерекомендуемый определяемый пользователем тип
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 1a32d98f5d034c2673d42301b45379da1302ca7f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832087"
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