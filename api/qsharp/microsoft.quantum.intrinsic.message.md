---
uid: Microsoft.Quantum.Intrinsic.Message
title: Функция Message
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849378"
---
# <a name="message-function"></a><span data-ttu-id="30340-102">Функция Message</span><span class="sxs-lookup"><span data-stu-id="30340-102">Message function</span></span>

<span data-ttu-id="30340-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="30340-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="30340-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="30340-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="30340-105">Записывает в журнал сообщение.</span><span class="sxs-lookup"><span data-stu-id="30340-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="30340-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="30340-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="30340-107">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="30340-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="30340-108">Сообщение, которое необходимо сообщить.</span><span class="sxs-lookup"><span data-stu-id="30340-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30340-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30340-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="30340-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="30340-110">Remarks</span></span>

<span data-ttu-id="30340-111">Конкретное поведение этой функции зависит от симулятора, но в большинстве случаев данное сообщение будет записано в консоль.</span><span class="sxs-lookup"><span data-stu-id="30340-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>