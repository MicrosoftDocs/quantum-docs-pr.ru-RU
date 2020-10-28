---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Функция Оператионповк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: f3c51410fb7c091385b64a1c4c99b3972d5055b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715691"
---
# <a name="operationpowc-function"></a><span data-ttu-id="543ca-102">Функция Оператионповк</span><span class="sxs-lookup"><span data-stu-id="543ca-102">OperationPowC function</span></span>

<span data-ttu-id="543ca-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="543ca-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="543ca-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="543ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="543ca-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="543ca-105">Raises an operation to a power.</span></span>
<span data-ttu-id="543ca-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="543ca-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="543ca-107">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="543ca-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="543ca-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="543ca-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="543ca-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="543ca-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="543ca-110">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="543ca-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="543ca-111">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="543ca-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="543ca-112">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="543ca-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="543ca-113">Выходные данные: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="543ca-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="543ca-114">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="543ca-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="543ca-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="543ca-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="543ca-116">Е</span><span class="sxs-lookup"><span data-stu-id="543ca-116">'T</span></span>

<span data-ttu-id="543ca-117">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="543ca-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="543ca-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="543ca-118">See Also</span></span>

- [<span data-ttu-id="543ca-119">Microsoft. тактов. Canon. Оператионпов</span><span class="sxs-lookup"><span data-stu-id="543ca-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)