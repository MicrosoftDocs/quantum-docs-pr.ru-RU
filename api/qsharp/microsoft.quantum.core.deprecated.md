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
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="a5f0a-102">Нерекомендуемый определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="a5f0a-102">Deprecated user defined type</span></span>

<span data-ttu-id="a5f0a-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a5f0a-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a5f0a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a5f0a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a5f0a-105">Распознанный компилятором атрибут, используемый для пометки типа или вызываемого как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="a5f0a-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="a5f0a-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="a5f0a-107">NewName: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a5f0a-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a5f0a-108">Полное имя типа или вызываемого для использования.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="a5f0a-109">Параметру присваивается пустая строка, если тип или вызываемый объект не рекомендуется использовать без подстановки.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>