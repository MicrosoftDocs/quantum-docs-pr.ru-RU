---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Операция Апплитореста
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 34cb5071dd939d0831e39bb8f1670670ae1fad31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208314"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="d479a-102">Операция Апплитореста</span><span class="sxs-lookup"><span data-stu-id="d479a-102">ApplyToRestA operation</span></span>

<span data-ttu-id="d479a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d479a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d479a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d479a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d479a-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="d479a-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="d479a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d479a-106">Description</span></span>

<span data-ttu-id="d479a-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d479a-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d479a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d479a-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="d479a-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="d479a-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d479a-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="d479a-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d479a-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="d479a-111">targets : 'T[]</span></span>

<span data-ttu-id="d479a-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="d479a-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d479a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d479a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d479a-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d479a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d479a-115">Е</span><span class="sxs-lookup"><span data-stu-id="d479a-115">'T</span></span>

<span data-ttu-id="d479a-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="d479a-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d479a-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="d479a-117">See Also</span></span>

- [<span data-ttu-id="d479a-118">Microsoft. тактов. Canon. Апплиторест</span><span class="sxs-lookup"><span data-stu-id="d479a-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="d479a-119">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="d479a-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="d479a-120">Microsoft. тактов. Canon. Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="d479a-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)