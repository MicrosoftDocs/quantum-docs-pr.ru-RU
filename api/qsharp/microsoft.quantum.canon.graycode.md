---
uid: Microsoft.Quantum.Canon.GrayCode
title: Функция Грайкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716167"
---
# <a name="graycode-function"></a><span data-ttu-id="a69b1-102">Функция Грайкоде</span><span class="sxs-lookup"><span data-stu-id="a69b1-102">GrayCode function</span></span>

<span data-ttu-id="a69b1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a69b1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a69b1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a69b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a69b1-105">Создает серые последовательности кода</span><span class="sxs-lookup"><span data-stu-id="a69b1-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="a69b1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a69b1-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="a69b1-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a69b1-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a69b1-108">Число битов</span><span class="sxs-lookup"><span data-stu-id="a69b1-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="a69b1-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="a69b1-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="a69b1-110">Массив кортежей.</span><span class="sxs-lookup"><span data-stu-id="a69b1-110">Array of tuples.</span></span> <span data-ttu-id="a69b1-111">Первое значение кортежа является значением во втором значении последовательности Грайкоде в кортеже, которое изменяется в текущем значении для получения следующего.</span><span class="sxs-lookup"><span data-stu-id="a69b1-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>