---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Функция Рменкодинг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202946"
---
# <a name="rmencoding-function"></a><span data-ttu-id="7d97b-102">Функция Рменкодинг</span><span class="sxs-lookup"><span data-stu-id="7d97b-102">RMEncoding function</span></span>

<span data-ttu-id="7d97b-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7d97b-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7d97b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d97b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d97b-105">{-1,1} кодирование логического значения истинности</span><span class="sxs-lookup"><span data-stu-id="7d97b-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="7d97b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7d97b-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="7d97b-107">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="7d97b-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7d97b-108">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="7d97b-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="7d97b-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7d97b-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7d97b-110">1, если `b` имеет значение false, в противном случае — 1.</span><span class="sxs-lookup"><span data-stu-id="7d97b-110">1, if `b` is false, otherwise -1</span></span>