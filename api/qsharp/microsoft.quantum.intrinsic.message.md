---
uid: Microsoft.Quantum.Intrinsic.Message
title: Функция Message
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 0428a46bc639bc8a0697f5bd392f85b8b9f40ee5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711422"
---
# <a name="message-function"></a><span data-ttu-id="44f34-102">Функция Message</span><span class="sxs-lookup"><span data-stu-id="44f34-102">Message function</span></span>

<span data-ttu-id="44f34-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="44f34-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="44f34-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="44f34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="44f34-105">Записывает в журнал сообщение.</span><span class="sxs-lookup"><span data-stu-id="44f34-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="44f34-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="44f34-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="44f34-107">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="44f34-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="44f34-108">Сообщение, которое необходимо сообщить.</span><span class="sxs-lookup"><span data-stu-id="44f34-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="44f34-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="44f34-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="44f34-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="44f34-110">Remarks</span></span>

<span data-ttu-id="44f34-111">Конкретное поведение этой функции зависит от симулятора, но в большинстве случаев данное сообщение будет записано в консоль.</span><span class="sxs-lookup"><span data-stu-id="44f34-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>