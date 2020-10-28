---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Функция фактов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 6a08703f68f9f38f2224fe4c6a4d255b00756908
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712682"
---
# <a name="fact-function"></a><span data-ttu-id="367e9-102">Функция фактов</span><span class="sxs-lookup"><span data-stu-id="367e9-102">Fact function</span></span>

<span data-ttu-id="367e9-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="367e9-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="367e9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="367e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="367e9-105">Объявляет, что классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="367e9-105">Declares that a classical condition is true.</span></span>

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="367e9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="367e9-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="367e9-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="367e9-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="367e9-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="367e9-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="367e9-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="367e9-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="367e9-110">Строка сообщения об ошибке для печати в случае, если классический параметр имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="367e9-110">Failure message string to be printed in the case that the classical condition is false.</span></span>



## <a name="output--unit"></a><span data-ttu-id="367e9-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="367e9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="367e9-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="367e9-112">See Also</span></span>

- [<span data-ttu-id="367e9-113">Microsoft. тактов. Diagnostics. противоречит</span><span class="sxs-lookup"><span data-stu-id="367e9-113">Microsoft.Quantum.Diagnostics.Contradiction</span></span>](xref:Microsoft.Quantum.Diagnostics.Contradiction)