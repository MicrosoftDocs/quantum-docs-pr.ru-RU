---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Операция Апплиторестк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 1e533a9f0994b70054aeca2f9ddd97f4e200b03f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850497"
---
# <a name="applytorestc-operation"></a><span data-ttu-id="eff4d-102">Операция Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="eff4d-102">ApplyToRestC operation</span></span>

<span data-ttu-id="eff4d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eff4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eff4d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eff4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eff4d-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="eff4d-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="eff4d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="eff4d-106">Description</span></span>

<span data-ttu-id="eff4d-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="eff4d-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="eff4d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eff4d-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="eff4d-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="eff4d-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="eff4d-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="eff4d-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="eff4d-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="eff4d-111">targets : 'T[]</span></span>

<span data-ttu-id="eff4d-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="eff4d-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eff4d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eff4d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eff4d-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="eff4d-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eff4d-115">Е</span><span class="sxs-lookup"><span data-stu-id="eff4d-115">'T</span></span>

<span data-ttu-id="eff4d-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="eff4d-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="eff4d-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="eff4d-117">See Also</span></span>

- [<span data-ttu-id="eff4d-118">Microsoft. тактов. Canon. Апплиторест</span><span class="sxs-lookup"><span data-stu-id="eff4d-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="eff4d-119">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="eff4d-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="eff4d-120">Microsoft. тактов. Canon. Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="eff4d-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)