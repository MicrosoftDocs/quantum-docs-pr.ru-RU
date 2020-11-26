---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Функция Сизеаджустедтрустабле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202929"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="cc1a4-102">Функция Сизеаджустедтрустабле</span><span class="sxs-lookup"><span data-stu-id="cc1a4-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="cc1a4-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="cc1a4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="cc1a4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc1a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc1a4-105">Корректирует таблицу истинности из массива логических значений в соответствии с количеством переменных</span><span class="sxs-lookup"><span data-stu-id="cc1a4-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="cc1a4-106">Новый массив возвращается длиной `2^numVars` , возможно, требуется расширить `table` размер с помощью `false` записей или усечь его до `2^numVars` элементов.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="cc1a4-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cc1a4-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="cc1a4-108">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cc1a4-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cc1a4-109">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="cc1a4-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="cc1a4-110">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cc1a4-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cc1a4-111">Число переменных</span><span class="sxs-lookup"><span data-stu-id="cc1a4-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="cc1a4-112">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cc1a4-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cc1a4-113">Таблица скорректированных размеров</span><span class="sxs-lookup"><span data-stu-id="cc1a4-113">Size adjusted truth table</span></span>