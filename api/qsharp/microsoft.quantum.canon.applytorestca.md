---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Операция Апплиторестка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208165"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="8a4b3-102">Операция Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="8a4b3-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="8a4b3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8a4b3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8a4b3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8a4b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8a4b3-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="8a4b3-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8a4b3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8a4b3-106">Description</span></span>

<span data-ttu-id="8a4b3-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="8a4b3-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="8a4b3-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8a4b3-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="8a4b3-109">Op: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="8a4b3-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8a4b3-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="8a4b3-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="8a4b3-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="8a4b3-111">targets : 'T[]</span></span>

<span data-ttu-id="8a4b3-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="8a4b3-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8a4b3-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8a4b3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8a4b3-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8a4b3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8a4b3-115">Е</span><span class="sxs-lookup"><span data-stu-id="8a4b3-115">'T</span></span>

<span data-ttu-id="8a4b3-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="8a4b3-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a4b3-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="8a4b3-117">See Also</span></span>

- [<span data-ttu-id="8a4b3-118">Microsoft. тактов. Canon. Апплиторест</span><span class="sxs-lookup"><span data-stu-id="8a4b3-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="8a4b3-119">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="8a4b3-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="8a4b3-120">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="8a4b3-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)