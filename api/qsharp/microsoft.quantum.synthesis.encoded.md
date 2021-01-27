---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Encoded, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855494"
---
# <a name="encoded-function"></a><span data-ttu-id="318be-102">Encoded, функция</span><span class="sxs-lookup"><span data-stu-id="318be-102">Encoded function</span></span>

<span data-ttu-id="318be-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="318be-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="318be-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="318be-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="318be-105">Кодирование таблицы истинности в {1,-1} коде</span><span class="sxs-lookup"><span data-stu-id="318be-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="318be-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="318be-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="318be-107">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="318be-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="318be-108">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="318be-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="318be-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="318be-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="318be-110">Истинная таблица в виде массива {1,-1} целых чисел</span><span class="sxs-lookup"><span data-stu-id="318be-110">Truth table as array of {1,-1} integers</span></span>

## <a name="example"></a><span data-ttu-id="318be-111">Пример</span><span class="sxs-lookup"><span data-stu-id="318be-111">Example</span></span>

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```