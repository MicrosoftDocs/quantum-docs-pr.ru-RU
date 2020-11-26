---
uid: Microsoft.Quantum.Intrinsic.Message
title: Функция Message
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199018"
---
# <a name="message-function"></a><span data-ttu-id="2efdb-102">Функция Message</span><span class="sxs-lookup"><span data-stu-id="2efdb-102">Message function</span></span>

<span data-ttu-id="2efdb-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="2efdb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="2efdb-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2efdb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2efdb-105">Записывает в журнал сообщение.</span><span class="sxs-lookup"><span data-stu-id="2efdb-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="2efdb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2efdb-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="2efdb-107">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2efdb-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="2efdb-108">Сообщение, которое необходимо сообщить.</span><span class="sxs-lookup"><span data-stu-id="2efdb-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2efdb-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2efdb-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2efdb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2efdb-110">Remarks</span></span>

<span data-ttu-id="2efdb-111">Конкретное поведение этой функции зависит от симулятора, но в большинстве случаев данное сообщение будет записано в консоль.</span><span class="sxs-lookup"><span data-stu-id="2efdb-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>