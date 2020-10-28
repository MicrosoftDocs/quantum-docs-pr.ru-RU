---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Функция Форматтедфаилуре
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712681"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="6867d-102">Функция Форматтедфаилуре</span><span class="sxs-lookup"><span data-stu-id="6867d-102">FormattedFailure function</span></span>

<span data-ttu-id="6867d-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6867d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6867d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6867d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6867d-105">Внутренняя функция, используемая для сбоя с осмысленными сообщениями об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6867d-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="6867d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6867d-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="6867d-107">фактический: нет</span><span class="sxs-lookup"><span data-stu-id="6867d-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="6867d-108">ожидалось: 'T</span><span class="sxs-lookup"><span data-stu-id="6867d-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="6867d-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="6867d-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="6867d-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6867d-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6867d-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6867d-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6867d-112">Е</span><span class="sxs-lookup"><span data-stu-id="6867d-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="6867d-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="6867d-113">Remarks</span></span>

<span data-ttu-id="6867d-114">Эта функция предназначена для имитации средой выполнения моделирования, поэтому она позволяет пересылать необработанные соответствия.</span><span class="sxs-lookup"><span data-stu-id="6867d-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>