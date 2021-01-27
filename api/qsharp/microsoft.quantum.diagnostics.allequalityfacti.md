---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Функция Аллекуалитифакти
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: a7043b9c670f79e270180c583fef56b70c1a3bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830887"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="40a22-102">Функция Аллекуалитифакти</span><span class="sxs-lookup"><span data-stu-id="40a22-102">AllEqualityFactI function</span></span>

<span data-ttu-id="40a22-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="40a22-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="40a22-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40a22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40a22-105">Утверждает, что два массива целочисленных значений равны.</span><span class="sxs-lookup"><span data-stu-id="40a22-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="40a22-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40a22-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="40a22-107">фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40a22-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40a22-108">Массив, создаваемый тестовым случаем.</span><span class="sxs-lookup"><span data-stu-id="40a22-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="40a22-109">ожидалось: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40a22-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40a22-110">Массив, который ожидается из тестового случая, представляющего интерес.</span><span class="sxs-lookup"><span data-stu-id="40a22-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="40a22-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="40a22-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="40a22-112">Выводимое сообщение, если массивы не равны.</span><span class="sxs-lookup"><span data-stu-id="40a22-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40a22-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40a22-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

