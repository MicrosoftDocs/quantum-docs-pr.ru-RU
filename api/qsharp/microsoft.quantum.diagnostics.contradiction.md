---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Функция противоречит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: f9ad9a7d67bda8e50c76f679f535ad55ba07698e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202147"
---
# <a name="contradiction-function"></a><span data-ttu-id="13109-102">Функция противоречит</span><span class="sxs-lookup"><span data-stu-id="13109-102">Contradiction function</span></span>

<span data-ttu-id="13109-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="13109-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="13109-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="13109-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="13109-105">Объявляет, что классическое условие имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="13109-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="13109-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="13109-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="13109-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="13109-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="13109-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="13109-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="13109-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="13109-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="13109-110">Строка сообщения об ошибке для печати в случае, если классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="13109-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13109-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13109-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="13109-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="13109-112">See Also</span></span>

- [<span data-ttu-id="13109-113">Microsoft. тактов. Diagnostics. факт</span><span class="sxs-lookup"><span data-stu-id="13109-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)