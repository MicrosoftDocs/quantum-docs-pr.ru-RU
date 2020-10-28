---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Функция Ископримел
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 7c077d508c93672d58a52a1403b3c5d73df75471
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732249"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="b335d-102">Функция Ископримел</span><span class="sxs-lookup"><span data-stu-id="b335d-102">IsCoprimeL function</span></span>

<span data-ttu-id="b335d-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b335d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b335d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b335d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b335d-105">Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b335d-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="b335d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b335d-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="b335d-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b335d-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b335d-108">Первое число, для которого проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="b335d-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="b335d-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b335d-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b335d-110">второе число, на которое проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="b335d-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="b335d-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b335d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b335d-112">True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае</span><span class="sxs-lookup"><span data-stu-id="b335d-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>