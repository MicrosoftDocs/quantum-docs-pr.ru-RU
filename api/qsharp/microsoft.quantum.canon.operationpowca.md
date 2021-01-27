---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Функция Оператионповка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 338c40f8eb9d6f1782989f2a91c86df561d480bf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852308"
---
# <a name="operationpowca-function"></a><span data-ttu-id="dbe59-102">Функция Оператионповка</span><span class="sxs-lookup"><span data-stu-id="dbe59-102">OperationPowCA function</span></span>

<span data-ttu-id="dbe59-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dbe59-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dbe59-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dbe59-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dbe59-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="dbe59-105">Raises an operation to a power.</span></span>
<span data-ttu-id="dbe59-106">Модификатор `A` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="dbe59-106">The modifier `A` indicates that the operation is controllable and adjointable.</span></span>

<span data-ttu-id="dbe59-107">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="dbe59-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="dbe59-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dbe59-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="dbe59-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="dbe59-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dbe59-110">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="dbe59-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="dbe59-111">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dbe59-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dbe59-112">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="dbe59-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="dbe59-113">Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL</span><span class="sxs-lookup"><span data-stu-id="dbe59-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dbe59-114">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="dbe59-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dbe59-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="dbe59-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dbe59-116">Е</span><span class="sxs-lookup"><span data-stu-id="dbe59-116">'T</span></span>

<span data-ttu-id="dbe59-117">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="dbe59-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe59-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="dbe59-118">See Also</span></span>

- [<span data-ttu-id="dbe59-119">Microsoft. тактов. Canon. Оператионпов</span><span class="sxs-lookup"><span data-stu-id="dbe59-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)