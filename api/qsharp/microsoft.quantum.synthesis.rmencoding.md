---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Функция Рменкодинг
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: ef9be0f0628c8ba8c5f131cc558bdcda6bb6ea55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734064"
---
# <a name="rmencoding-function"></a><span data-ttu-id="874e5-102">Функция Рменкодинг</span><span class="sxs-lookup"><span data-stu-id="874e5-102">RMEncoding function</span></span>

<span data-ttu-id="874e5-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="874e5-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="874e5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="874e5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="874e5-105">{-1,1} кодирование логического значения истинности</span><span class="sxs-lookup"><span data-stu-id="874e5-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="874e5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="874e5-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="874e5-107">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="874e5-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="874e5-108">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="874e5-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="874e5-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="874e5-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="874e5-110">1, если `b` имеет значение false, в противном случае — 1.</span><span class="sxs-lookup"><span data-stu-id="874e5-110">1, if `b` is false, otherwise -1</span></span>