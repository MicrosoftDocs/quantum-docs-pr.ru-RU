---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Функция Рменкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855343"
---
# <a name="rmencoding-function"></a><span data-ttu-id="a8519-102">Функция Рменкодинг</span><span class="sxs-lookup"><span data-stu-id="a8519-102">RMEncoding function</span></span>

<span data-ttu-id="a8519-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="a8519-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="a8519-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8519-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8519-105">{-1,1} кодирование логического значения истинности</span><span class="sxs-lookup"><span data-stu-id="a8519-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="a8519-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a8519-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="a8519-107">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="a8519-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a8519-108">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="a8519-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="a8519-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a8519-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a8519-110">1, если `b` имеет значение false, в противном случае — 1.</span><span class="sxs-lookup"><span data-stu-id="a8519-110">1, if `b` is false, otherwise -1</span></span>