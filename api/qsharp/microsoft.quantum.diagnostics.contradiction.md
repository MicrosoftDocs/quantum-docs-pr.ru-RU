---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Функция противоречит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829368"
---
# <a name="contradiction-function"></a><span data-ttu-id="8da3c-102">Функция противоречит</span><span class="sxs-lookup"><span data-stu-id="8da3c-102">Contradiction function</span></span>

<span data-ttu-id="8da3c-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8da3c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8da3c-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8da3c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8da3c-105">Объявляет, что классическое условие имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="8da3c-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="8da3c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8da3c-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="8da3c-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8da3c-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8da3c-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="8da3c-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="8da3c-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8da3c-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8da3c-110">Строка сообщения об ошибке для печати в случае, если классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="8da3c-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8da3c-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8da3c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="8da3c-112">Пример</span><span class="sxs-lookup"><span data-stu-id="8da3c-112">Example</span></span>

<span data-ttu-id="8da3c-113">Следующий код Q # выполнит печать "Hello, World":</span><span class="sxs-lookup"><span data-stu-id="8da3c-113">The following Q# code will print "Hello, world":</span></span>

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a><span data-ttu-id="8da3c-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="8da3c-114">See Also</span></span>

- [<span data-ttu-id="8da3c-115">Microsoft. тактов. Diagnostics. факт</span><span class="sxs-lookup"><span data-stu-id="8da3c-115">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)