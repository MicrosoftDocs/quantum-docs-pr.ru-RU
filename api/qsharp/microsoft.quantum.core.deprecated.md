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
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="e43ce-102">Нерекомендуемый определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="e43ce-102">Deprecated user defined type</span></span>

<span data-ttu-id="e43ce-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e43ce-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e43ce-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e43ce-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e43ce-105">Распознанный компилятором атрибут, используемый для пометки типа или вызываемого как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="e43ce-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="e43ce-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="e43ce-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="e43ce-107">NewName: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e43ce-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e43ce-108">Полное имя типа или вызываемого для использования.</span><span class="sxs-lookup"><span data-stu-id="e43ce-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="e43ce-109">Параметру присваивается пустая строка, если тип или вызываемый объект не рекомендуется использовать без подстановки.</span><span class="sxs-lookup"><span data-stu-id="e43ce-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>