---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Функция противоречит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712864"
---
# <a name="contradiction-function"></a><span data-ttu-id="e53d4-102">Функция противоречит</span><span class="sxs-lookup"><span data-stu-id="e53d4-102">Contradiction function</span></span>

<span data-ttu-id="e53d4-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e53d4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e53d4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e53d4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e53d4-105">Объявляет, что классическое условие имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="e53d4-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="e53d4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e53d4-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="e53d4-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e53d4-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e53d4-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="e53d4-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="e53d4-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e53d4-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e53d4-110">Строка сообщения об ошибке для печати в случае, если классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="e53d4-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e53d4-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e53d4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e53d4-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="e53d4-112">See Also</span></span>

- [<span data-ttu-id="e53d4-113">Microsoft. тактов. Diagnostics. факт</span><span class="sxs-lookup"><span data-stu-id="e53d4-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)