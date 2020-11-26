---
uid: Microsoft.Quantum.Canon.OperationPow
title: Функция Оператионпов
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 808001200d276ca21cc5a70140d5d84d96da3496
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205819"
---
# <a name="operationpow-function"></a><span data-ttu-id="b607b-102">Функция Оператионпов</span><span class="sxs-lookup"><span data-stu-id="b607b-102">OperationPow function</span></span>

<span data-ttu-id="b607b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b607b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b607b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b607b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b607b-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="b607b-105">Raises an operation to a power.</span></span>

<span data-ttu-id="b607b-106">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="b607b-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="b607b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b607b-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="b607b-108">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="b607b-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b607b-109">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="b607b-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="b607b-110">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b607b-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b607b-111">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="b607b-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="b607b-112">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b607b-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b607b-113">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="b607b-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b607b-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b607b-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b607b-115">Е</span><span class="sxs-lookup"><span data-stu-id="b607b-115">'T</span></span>

<span data-ttu-id="b607b-116">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="b607b-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="b607b-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="b607b-117">See Also</span></span>

- [<span data-ttu-id="b607b-118">Microsoft. тактов. Canon. Оператионповк</span><span class="sxs-lookup"><span data-stu-id="b607b-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="b607b-119">Microsoft. тактов. Canon. Оператионпова</span><span class="sxs-lookup"><span data-stu-id="b607b-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="b607b-120">Microsoft. тактов. Canon. Оператионповка</span><span class="sxs-lookup"><span data-stu-id="b607b-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)