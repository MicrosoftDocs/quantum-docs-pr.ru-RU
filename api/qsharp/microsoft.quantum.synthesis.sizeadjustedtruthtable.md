---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Функция Сизеаджустедтрустабле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 3480f022df7a289594b003f201d16d8bf7c29d7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734057"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="b72bc-102">Функция Сизеаджустедтрустабле</span><span class="sxs-lookup"><span data-stu-id="b72bc-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="b72bc-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b72bc-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b72bc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b72bc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b72bc-105">Корректирует таблицу истинности из массива логических значений в соответствии с количеством переменных</span><span class="sxs-lookup"><span data-stu-id="b72bc-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="b72bc-106">Новый массив возвращается длиной `2^numVars` , возможно, требуется расширить `table` размер с помощью `false` записей или усечь его до `2^numVars` элементов.</span><span class="sxs-lookup"><span data-stu-id="b72bc-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="b72bc-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b72bc-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="b72bc-108">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="b72bc-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="b72bc-109">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="b72bc-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="b72bc-110">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b72bc-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b72bc-111">Число переменных</span><span class="sxs-lookup"><span data-stu-id="b72bc-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="b72bc-112">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="b72bc-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="b72bc-113">Таблица скорректированных размеров</span><span class="sxs-lookup"><span data-stu-id="b72bc-113">Size adjusted truth table</span></span>