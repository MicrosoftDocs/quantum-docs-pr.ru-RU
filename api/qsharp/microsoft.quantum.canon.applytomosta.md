---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Операция Апплитомоста
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7c226de9b2c99d124c467175dfe65a60a89d4332
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208505"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="4495d-102">Операция Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="4495d-102">ApplyToMostA operation</span></span>

<span data-ttu-id="4495d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4495d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4495d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4495d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4495d-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="4495d-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="4495d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4495d-106">Description</span></span>

<span data-ttu-id="4495d-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="4495d-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="4495d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4495d-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="4495d-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="4495d-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4495d-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="4495d-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="4495d-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="4495d-111">targets : 'T[]</span></span>

<span data-ttu-id="4495d-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="4495d-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4495d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4495d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4495d-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4495d-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4495d-115">Е</span><span class="sxs-lookup"><span data-stu-id="4495d-115">'T</span></span>

<span data-ttu-id="4495d-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="4495d-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="4495d-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="4495d-117">See Also</span></span>

- [<span data-ttu-id="4495d-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="4495d-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="4495d-119">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="4495d-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="4495d-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="4495d-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)