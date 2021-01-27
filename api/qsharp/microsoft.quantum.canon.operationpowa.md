---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Функция Оператионпова
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 67491c3302392e9793677727606df1baaf4f205a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852355"
---
# <a name="operationpowa-function"></a><span data-ttu-id="ac9c1-102">Функция Оператионпова</span><span class="sxs-lookup"><span data-stu-id="ac9c1-102">OperationPowA function</span></span>

<span data-ttu-id="ac9c1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ac9c1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ac9c1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac9c1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac9c1-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-105">Raises an operation to a power.</span></span>
<span data-ttu-id="ac9c1-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="ac9c1-107">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="ac9c1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ac9c1-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="ac9c1-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="ac9c1-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ac9c1-110">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="ac9c1-111">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ac9c1-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ac9c1-112">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="ac9c1-113">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является прогода</span><span class="sxs-lookup"><span data-stu-id="ac9c1-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ac9c1-114">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ac9c1-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ac9c1-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ac9c1-116">Е</span><span class="sxs-lookup"><span data-stu-id="ac9c1-116">'T</span></span>

<span data-ttu-id="ac9c1-117">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac9c1-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="ac9c1-118">See Also</span></span>

- [<span data-ttu-id="ac9c1-119">Microsoft. тактов. Canon. Оператионпов</span><span class="sxs-lookup"><span data-stu-id="ac9c1-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)