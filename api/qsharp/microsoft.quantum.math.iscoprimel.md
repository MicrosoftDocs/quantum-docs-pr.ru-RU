---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Функция Ископримел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: a48f056d138499607d32b38b1fa0970745732c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851343"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="66cf2-102">Функция Ископримел</span><span class="sxs-lookup"><span data-stu-id="66cf2-102">IsCoprimeL function</span></span>

<span data-ttu-id="66cf2-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="66cf2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="66cf2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66cf2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66cf2-105">Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="66cf2-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="66cf2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66cf2-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="66cf2-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="66cf2-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="66cf2-108">Первое число, для которого проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="66cf2-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="66cf2-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="66cf2-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="66cf2-110">второе число, на которое проверяется сопрималити</span><span class="sxs-lookup"><span data-stu-id="66cf2-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="66cf2-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66cf2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66cf2-112">True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае</span><span class="sxs-lookup"><span data-stu-id="66cf2-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>