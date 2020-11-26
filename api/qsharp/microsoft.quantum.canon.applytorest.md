---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Операция Апплиторест
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: fe49361f3c2259960eaa58d47df9b69b30b572a8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208277"
---
# <a name="applytorest-operation"></a><span data-ttu-id="5198c-102">Операция Апплиторест</span><span class="sxs-lookup"><span data-stu-id="5198c-102">ApplyToRest operation</span></span>

<span data-ttu-id="5198c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5198c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5198c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5198c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5198c-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="5198c-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5198c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5198c-106">Description</span></span>

<span data-ttu-id="5198c-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5198c-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5198c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5198c-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="5198c-109">Op: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="5198c-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5198c-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="5198c-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5198c-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="5198c-111">targets : 'T[]</span></span>

<span data-ttu-id="5198c-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="5198c-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5198c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5198c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5198c-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5198c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5198c-115">Е</span><span class="sxs-lookup"><span data-stu-id="5198c-115">'T</span></span>

<span data-ttu-id="5198c-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="5198c-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5198c-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="5198c-117">See Also</span></span>

- [<span data-ttu-id="5198c-118">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="5198c-118">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="5198c-119">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="5198c-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="5198c-120">Microsoft. тактов. Canon. Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="5198c-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)