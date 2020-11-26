---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Функция Аллекуалитифакти
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 92b57f49407d558e5f8d0365c168b7890f1f4981
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223890"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="8c4f8-102">Функция Аллекуалитифакти</span><span class="sxs-lookup"><span data-stu-id="8c4f8-102">AllEqualityFactI function</span></span>

<span data-ttu-id="8c4f8-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8c4f8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8c4f8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8c4f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8c4f8-105">Утверждает, что два массива целочисленных значений равны.</span><span class="sxs-lookup"><span data-stu-id="8c4f8-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="8c4f8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8c4f8-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="8c4f8-107">фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8c4f8-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8c4f8-108">Массив, создаваемый тестовым случаем.</span><span class="sxs-lookup"><span data-stu-id="8c4f8-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="8c4f8-109">ожидалось: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8c4f8-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8c4f8-110">Массив, который ожидается из тестового случая, представляющего интерес.</span><span class="sxs-lookup"><span data-stu-id="8c4f8-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="8c4f8-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8c4f8-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8c4f8-112">Выводимое сообщение, если массивы не равны.</span><span class="sxs-lookup"><span data-stu-id="8c4f8-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8c4f8-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c4f8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

