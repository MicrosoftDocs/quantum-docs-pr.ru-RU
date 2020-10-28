---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Encoded, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 6b9d21969ee90f3928b65a1c97a5b0f15157e381
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733905"
---
# <a name="encoded-function"></a><span data-ttu-id="55d99-102">Encoded, функция</span><span class="sxs-lookup"><span data-stu-id="55d99-102">Encoded function</span></span>

<span data-ttu-id="55d99-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="55d99-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="55d99-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="55d99-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="55d99-105">Кодирование таблицы истинности в {1,-1} коде</span><span class="sxs-lookup"><span data-stu-id="55d99-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="55d99-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="55d99-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="55d99-107">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="55d99-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="55d99-108">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="55d99-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="55d99-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="55d99-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="55d99-110">Истинная таблица в виде массива {1,-1} целых чисел</span><span class="sxs-lookup"><span data-stu-id="55d99-110">Truth table as array of {1,-1} integers</span></span>