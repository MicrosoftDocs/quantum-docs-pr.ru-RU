---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Функция Аллекуалитифакти
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 9ccd212010ae557de5ca4ab2a38d4724c5c29aa8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713073"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="e866f-102">Функция Аллекуалитифакти</span><span class="sxs-lookup"><span data-stu-id="e866f-102">AllEqualityFactI function</span></span>

<span data-ttu-id="e866f-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e866f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e866f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e866f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e866f-105">Утверждает, что два массива целочисленных значений равны.</span><span class="sxs-lookup"><span data-stu-id="e866f-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="e866f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e866f-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="e866f-107">фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e866f-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e866f-108">Массив, создаваемый тестовым случаем.</span><span class="sxs-lookup"><span data-stu-id="e866f-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="e866f-109">ожидалось: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e866f-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e866f-110">Массив, который ожидается из тестового случая, представляющего интерес.</span><span class="sxs-lookup"><span data-stu-id="e866f-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="e866f-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e866f-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e866f-112">Выводимое сообщение, если массивы не равны.</span><span class="sxs-lookup"><span data-stu-id="e866f-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e866f-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e866f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

