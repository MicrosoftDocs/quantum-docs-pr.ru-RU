---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Функция Ископримел
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: c78e995801f67822cf98104a7319093d853b6afe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228140"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="4a967-102">Функция Ископримел</span><span class="sxs-lookup"><span data-stu-id="4a967-102">IsCoprimeL function</span></span>

<span data-ttu-id="4a967-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4a967-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4a967-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a967-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a967-105">Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a967-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="4a967-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4a967-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="4a967-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4a967-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4a967-108">Первое число, для которого проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="4a967-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="4a967-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4a967-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4a967-110">второе число, на которое проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="4a967-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="4a967-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4a967-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4a967-112">True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае</span><span class="sxs-lookup"><span data-stu-id="4a967-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>