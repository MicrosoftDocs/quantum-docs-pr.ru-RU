---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Функция фактов
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 74ec020d0437d885d7cbfc98a2c9c0c1867d5d39
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201688"
---
# <a name="fact-function"></a><span data-ttu-id="7d91f-102">Функция фактов</span><span class="sxs-lookup"><span data-stu-id="7d91f-102">Fact function</span></span>

<span data-ttu-id="7d91f-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7d91f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7d91f-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7d91f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7d91f-105">Объявляет, что классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="7d91f-105">Declares that a classical condition is true.</span></span>

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="7d91f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7d91f-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="7d91f-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7d91f-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7d91f-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="7d91f-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="7d91f-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7d91f-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7d91f-110">Строка сообщения об ошибке для печати в случае, если классический параметр имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="7d91f-110">Failure message string to be printed in the case that the classical condition is false.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d91f-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d91f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="7d91f-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="7d91f-112">See Also</span></span>

- [<span data-ttu-id="7d91f-113">Microsoft. тактов. Diagnostics. противоречит</span><span class="sxs-lookup"><span data-stu-id="7d91f-113">Microsoft.Quantum.Diagnostics.Contradiction</span></span>](xref:Microsoft.Quantum.Diagnostics.Contradiction)