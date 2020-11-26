---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Функция Оператионпова
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 35dc76a06fd4e8c819b785fd4c588f108c918326
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205785"
---
# <a name="operationpowa-function"></a><span data-ttu-id="824da-102">Функция Оператионпова</span><span class="sxs-lookup"><span data-stu-id="824da-102">OperationPowA function</span></span>

<span data-ttu-id="824da-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="824da-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="824da-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="824da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="824da-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="824da-105">Raises an operation to a power.</span></span>
<span data-ttu-id="824da-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="824da-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="824da-107">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="824da-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="824da-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="824da-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="824da-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="824da-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="824da-110">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="824da-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="824da-111">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="824da-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="824da-112">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="824da-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="824da-113">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является прогода</span><span class="sxs-lookup"><span data-stu-id="824da-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="824da-114">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="824da-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="824da-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="824da-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="824da-116">Е</span><span class="sxs-lookup"><span data-stu-id="824da-116">'T</span></span>

<span data-ttu-id="824da-117">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="824da-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="824da-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="824da-118">See Also</span></span>

- [<span data-ttu-id="824da-119">Microsoft. тактов. Canon. Оператионпов</span><span class="sxs-lookup"><span data-stu-id="824da-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)