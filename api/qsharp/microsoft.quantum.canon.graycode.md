---
uid: Microsoft.Quantum.Canon.GrayCode
title: Функция Грайкоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206890"
---
# <a name="graycode-function"></a><span data-ttu-id="da886-102">Функция Грайкоде</span><span class="sxs-lookup"><span data-stu-id="da886-102">GrayCode function</span></span>

<span data-ttu-id="da886-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="da886-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="da886-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="da886-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="da886-105">Создает серые последовательности кода</span><span class="sxs-lookup"><span data-stu-id="da886-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="da886-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="da886-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="da886-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="da886-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="da886-108">Число битов</span><span class="sxs-lookup"><span data-stu-id="da886-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="da886-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="da886-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="da886-110">Массив кортежей.</span><span class="sxs-lookup"><span data-stu-id="da886-110">Array of tuples.</span></span> <span data-ttu-id="da886-111">Первое значение кортежа является значением во втором значении последовательности Грайкоде в кортеже, которое изменяется в текущем значении для получения следующего.</span><span class="sxs-lookup"><span data-stu-id="da886-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>