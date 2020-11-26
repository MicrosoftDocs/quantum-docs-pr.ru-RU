---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Функция Екуалитифактл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 2aaabf39d6ce49952466a877685776490ef438ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201807"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="6db35-102">Функция Екуалитифактл</span><span class="sxs-lookup"><span data-stu-id="6db35-102">EqualityFactL function</span></span>

<span data-ttu-id="6db35-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6db35-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6db35-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6db35-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6db35-105">Утверждает, что классическая переменная типа BigInt имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6db35-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="6db35-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6db35-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="6db35-107">фактический: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6db35-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6db35-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="6db35-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="6db35-109">ожидалось: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6db35-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6db35-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6db35-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="6db35-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="6db35-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="6db35-112">Строка сообщения об ошибке, используемая при срабатывании утверждения.</span><span class="sxs-lookup"><span data-stu-id="6db35-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6db35-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6db35-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

