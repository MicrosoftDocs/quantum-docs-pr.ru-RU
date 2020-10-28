---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Функция Ископримеи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: bdfaecb61f56967e21bf85ba190638b43685214d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732849"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="59015-102">Функция Ископримеи</span><span class="sxs-lookup"><span data-stu-id="59015-102">IsCoprimeI function</span></span>

<span data-ttu-id="59015-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="59015-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="59015-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59015-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59015-105">Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="59015-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="59015-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59015-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="59015-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="59015-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="59015-108">Первое число, для которого проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="59015-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="59015-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="59015-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="59015-110">второе число, на которое проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="59015-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="59015-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="59015-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="59015-112">True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае</span><span class="sxs-lookup"><span data-stu-id="59015-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>