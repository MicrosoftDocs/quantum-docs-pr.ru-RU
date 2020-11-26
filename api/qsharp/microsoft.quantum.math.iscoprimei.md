---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Функция Ископримеи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 53131a755571ad1ac0a8a984bf229b16f67dbe51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195364"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="004c4-102">Функция Ископримеи</span><span class="sxs-lookup"><span data-stu-id="004c4-102">IsCoprimeI function</span></span>

<span data-ttu-id="004c4-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="004c4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="004c4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="004c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="004c4-105">Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="004c4-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="004c4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="004c4-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="004c4-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="004c4-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="004c4-108">Первое число, для которого проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="004c4-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="004c4-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="004c4-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="004c4-110">второе число, на которое проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="004c4-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="004c4-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="004c4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="004c4-112">True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае</span><span class="sxs-lookup"><span data-stu-id="004c4-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>