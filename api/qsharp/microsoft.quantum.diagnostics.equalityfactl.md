---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Функция Екуалитифактл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 5e590af581be4e41df9d2081260409c454e3be4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712752"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="74dc0-102">Функция Екуалитифактл</span><span class="sxs-lookup"><span data-stu-id="74dc0-102">EqualityFactL function</span></span>

<span data-ttu-id="74dc0-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="74dc0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="74dc0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74dc0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74dc0-105">Утверждает, что классическая переменная типа BigInt имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="74dc0-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="74dc0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="74dc0-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="74dc0-107">фактический: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="74dc0-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="74dc0-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="74dc0-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="74dc0-109">ожидалось: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="74dc0-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="74dc0-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="74dc0-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="74dc0-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="74dc0-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="74dc0-112">Строка сообщения об ошибке, используемая при срабатывании утверждения.</span><span class="sxs-lookup"><span data-stu-id="74dc0-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74dc0-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74dc0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

