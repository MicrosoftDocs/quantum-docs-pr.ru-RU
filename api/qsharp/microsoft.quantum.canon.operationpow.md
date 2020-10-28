---
uid: Microsoft.Quantum.Canon.OperationPow
title: Функция Оператионпов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715775"
---
# <a name="operationpow-function"></a><span data-ttu-id="2c61d-102">Функция Оператионпов</span><span class="sxs-lookup"><span data-stu-id="2c61d-102">OperationPow function</span></span>

<span data-ttu-id="2c61d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2c61d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2c61d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2c61d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2c61d-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="2c61d-105">Raises an operation to a power.</span></span>

<span data-ttu-id="2c61d-106">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="2c61d-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="2c61d-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c61d-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="2c61d-108">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="2c61d-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2c61d-109">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="2c61d-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="2c61d-110">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c61d-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c61d-111">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="2c61d-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="2c61d-112">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c61d-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2c61d-113">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="2c61d-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2c61d-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2c61d-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2c61d-115">Е</span><span class="sxs-lookup"><span data-stu-id="2c61d-115">'T</span></span>

<span data-ttu-id="2c61d-116">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="2c61d-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c61d-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="2c61d-117">See Also</span></span>

- [<span data-ttu-id="2c61d-118">Microsoft. тактов. Canon. Оператионповк</span><span class="sxs-lookup"><span data-stu-id="2c61d-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="2c61d-119">Microsoft. тактов. Canon. Оператионпова</span><span class="sxs-lookup"><span data-stu-id="2c61d-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="2c61d-120">Microsoft. тактов. Canon. Оператионповка</span><span class="sxs-lookup"><span data-stu-id="2c61d-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)