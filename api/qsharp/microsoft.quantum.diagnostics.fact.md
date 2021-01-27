---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Функция фактов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853307"
---
# <a name="fact-function"></a><span data-ttu-id="374e5-102">Функция фактов</span><span class="sxs-lookup"><span data-stu-id="374e5-102">Fact function</span></span>

<span data-ttu-id="374e5-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="374e5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="374e5-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="374e5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="374e5-105">Объявляет, что классическое условие имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="374e5-105">Declares that a classical condition is true.</span></span>

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="374e5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="374e5-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="374e5-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="374e5-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="374e5-108">Условие, которое необходимо объявить.</span><span class="sxs-lookup"><span data-stu-id="374e5-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="374e5-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="374e5-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="374e5-110">Строка сообщения об ошибке для печати в случае, если классический параметр имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="374e5-110">Failure message string to be printed in the case that the classical condition is false.</span></span>



## <a name="output--unit"></a><span data-ttu-id="374e5-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="374e5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="374e5-112">Пример</span><span class="sxs-lookup"><span data-stu-id="374e5-112">Example</span></span>

<span data-ttu-id="374e5-113">Следующий фрагмент Q # завершится ошибкой:</span><span class="sxs-lookup"><span data-stu-id="374e5-113">The following Q# snippet will fail:</span></span>

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a><span data-ttu-id="374e5-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="374e5-114">See Also</span></span>

- [<span data-ttu-id="374e5-115">Microsoft. тактов. Diagnostics. противоречит</span><span class="sxs-lookup"><span data-stu-id="374e5-115">Microsoft.Quantum.Diagnostics.Contradiction</span></span>](xref:Microsoft.Quantum.Diagnostics.Contradiction)