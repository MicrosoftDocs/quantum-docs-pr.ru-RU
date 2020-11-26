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
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="f012d-102">Нерекомендуемый определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="f012d-102">Deprecated user defined type</span></span>

<span data-ttu-id="f012d-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="f012d-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="f012d-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f012d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f012d-105">Распознанный компилятором атрибут, используемый для пометки типа или вызываемого как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="f012d-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="f012d-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="f012d-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="f012d-107">NewName: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f012d-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f012d-108">Полное имя типа или вызываемого для использования.</span><span class="sxs-lookup"><span data-stu-id="f012d-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="f012d-109">Параметру присваивается пустая строка, если тип или вызываемый объект не рекомендуется использовать без подстановки.</span><span class="sxs-lookup"><span data-stu-id="f012d-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>