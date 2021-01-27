---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Функция Оператионповк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 05b0d5b286e16c308d8c3df8fb8fa1ac8c9868ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852353"
---
# <a name="operationpowc-function"></a><span data-ttu-id="93182-102">Функция Оператионповк</span><span class="sxs-lookup"><span data-stu-id="93182-102">OperationPowC function</span></span>

<span data-ttu-id="93182-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="93182-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="93182-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93182-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93182-105">Порождает операцию в степень.</span><span class="sxs-lookup"><span data-stu-id="93182-105">Raises an operation to a power.</span></span>
<span data-ttu-id="93182-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="93182-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="93182-107">То есть операция, представляющая шлюз $U $, возвращает новую операцию $U ^ m $ для Power $m $.</span><span class="sxs-lookup"><span data-stu-id="93182-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="93182-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="93182-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="93182-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="93182-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="93182-110">Операция $U $, представляющая шлюз, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="93182-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="93182-111">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="93182-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="93182-112">Количество повторных попыток $U $.</span><span class="sxs-lookup"><span data-stu-id="93182-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="93182-113">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="93182-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="93182-114">Новая операция, представляющая $U ^ m $, где $m = \тексттт{повер} $.</span><span class="sxs-lookup"><span data-stu-id="93182-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="93182-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="93182-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="93182-116">Е</span><span class="sxs-lookup"><span data-stu-id="93182-116">'T</span></span>

<span data-ttu-id="93182-117">Тип операции, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="93182-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="93182-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="93182-118">See Also</span></span>

- [<span data-ttu-id="93182-119">Microsoft. тактов. Canon. Оператионпов</span><span class="sxs-lookup"><span data-stu-id="93182-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)