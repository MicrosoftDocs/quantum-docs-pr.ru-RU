---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Функция Екуалитифактб
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: d3163281772bda392fbdd61ad58543e22022a600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712779"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="ad890-102">Функция Екуалитифактб</span><span class="sxs-lookup"><span data-stu-id="ad890-102">EqualityFactB function</span></span>

<span data-ttu-id="ad890-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ad890-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ad890-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad890-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad890-105">Утверждает, что классическая bool-переменная имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="ad890-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="ad890-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad890-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="ad890-107">фактический: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ad890-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ad890-108">Проверяемая переменная.</span><span class="sxs-lookup"><span data-stu-id="ad890-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="ad890-109">Ожидается: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ad890-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ad890-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="ad890-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="ad890-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="ad890-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="ad890-112">Строка сообщения об ошибке, используемая при срабатывании утверждения.</span><span class="sxs-lookup"><span data-stu-id="ad890-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ad890-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad890-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

