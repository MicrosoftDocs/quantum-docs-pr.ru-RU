---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Функция Форматтедфаилуре
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: da809c04059d4fd0f0ec92412a3094f5b582fd91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201705"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="2a566-102">Функция Форматтедфаилуре</span><span class="sxs-lookup"><span data-stu-id="2a566-102">FormattedFailure function</span></span>

<span data-ttu-id="2a566-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2a566-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2a566-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a566-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a566-105">Внутренняя функция, используемая для сбоя с осмысленными сообщениями об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2a566-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="2a566-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a566-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="2a566-107">фактический: нет</span><span class="sxs-lookup"><span data-stu-id="2a566-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="2a566-108">ожидалось: 'T</span><span class="sxs-lookup"><span data-stu-id="2a566-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="2a566-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2a566-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="2a566-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a566-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2a566-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2a566-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a566-112">Е</span><span class="sxs-lookup"><span data-stu-id="2a566-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="2a566-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a566-113">Remarks</span></span>

<span data-ttu-id="2a566-114">Эта функция предназначена для имитации средой выполнения моделирования, поэтому она позволяет пересылать необработанные соответствия.</span><span class="sxs-lookup"><span data-stu-id="2a566-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>