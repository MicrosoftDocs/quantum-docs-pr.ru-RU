---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Функция Сизеаджустедтрустабле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 8d69aa119c25a0f64743fec36c00ecdef2450c44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855319"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="5f61e-102">Функция Сизеаджустедтрустабле</span><span class="sxs-lookup"><span data-stu-id="5f61e-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="5f61e-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5f61e-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5f61e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f61e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f61e-105">Корректирует таблицу истинности из массива логических значений в соответствии с количеством переменных</span><span class="sxs-lookup"><span data-stu-id="5f61e-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="5f61e-106">Новый массив возвращается длиной `2^numVars` , возможно, требуется расширить `table` размер с помощью `false` записей или усечь его до `2^numVars` элементов.</span><span class="sxs-lookup"><span data-stu-id="5f61e-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="5f61e-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5f61e-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="5f61e-108">Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5f61e-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5f61e-109">Истинная таблица как массив значений истинности</span><span class="sxs-lookup"><span data-stu-id="5f61e-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="5f61e-110">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5f61e-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5f61e-111">Число переменных</span><span class="sxs-lookup"><span data-stu-id="5f61e-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="5f61e-112">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5f61e-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5f61e-113">Таблица скорректированных размеров</span><span class="sxs-lookup"><span data-stu-id="5f61e-113">Size adjusted truth table</span></span>