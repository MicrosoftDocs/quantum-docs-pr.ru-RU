---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Encoded, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 803f35b9e7af547bc34f21de74684fba885bfda9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203184"
---
# <a name="encoded-function"></a><span data-ttu-id="01d9a-102">Encoded, функция</span><span class="sxs-lookup"><span data-stu-id="01d9a-102">Encoded function</span></span>

<span data-ttu-id="01d9a-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="01d9a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="01d9a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="01d9a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="01d9a-105">Кодирование таблицы истинности в {1,-1} коде</span><span class="sxs-lookup"><span data-stu-id="01d9a-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="01d9a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="01d9a-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="01d9a-107">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="01d9a-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="01d9a-108">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="01d9a-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="01d9a-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="01d9a-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="01d9a-110">Истинная таблица в виде массива {1,-1} целых чисел</span><span class="sxs-lookup"><span data-stu-id="01d9a-110">Truth table as array of {1,-1} integers</span></span>