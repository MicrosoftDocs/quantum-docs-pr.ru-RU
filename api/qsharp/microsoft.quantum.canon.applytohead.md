---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Операция Апплитохеад
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e627b467e9354e774c2ead8b89ddd3ff3a42ef7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841335"
---
# <a name="applytohead-operation"></a><span data-ttu-id="5f3fe-102">Операция Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="5f3fe-102">ApplyToHead operation</span></span>

<span data-ttu-id="5f3fe-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5f3fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5f3fe-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f3fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f3fe-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="5f3fe-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5f3fe-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5f3fe-106">Description</span></span>

<span data-ttu-id="5f3fe-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5f3fe-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5f3fe-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5f3fe-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="5f3fe-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="5f3fe-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5f3fe-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="5f3fe-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5f3fe-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="5f3fe-111">targets : 'T[]</span></span>

<span data-ttu-id="5f3fe-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="5f3fe-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5f3fe-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5f3fe-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5f3fe-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5f3fe-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5f3fe-115">Е</span><span class="sxs-lookup"><span data-stu-id="5f3fe-115">'T</span></span>

<span data-ttu-id="5f3fe-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="5f3fe-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="5f3fe-117">Пример</span><span class="sxs-lookup"><span data-stu-id="5f3fe-117">Example</span></span>

<span data-ttu-id="5f3fe-118">Следующие фрагменты кода Q # эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5f3fe-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToHead(H, register);
H(Head(register));
```

## <a name="see-also"></a><span data-ttu-id="5f3fe-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="5f3fe-119">See Also</span></span>

- [<span data-ttu-id="5f3fe-120">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="5f3fe-120">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="5f3fe-121">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="5f3fe-121">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="5f3fe-122">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="5f3fe-122">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)