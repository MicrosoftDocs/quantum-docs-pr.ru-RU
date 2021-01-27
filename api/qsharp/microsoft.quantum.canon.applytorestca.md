---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Операция Апплиторестка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: e64eeaae2151a28c289e3e71e47f897d6c378b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841246"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="ed0bd-102">Операция Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="ed0bd-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="ed0bd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ed0bd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ed0bd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed0bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed0bd-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="ed0bd-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ed0bd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ed0bd-106">Description</span></span>

<span data-ttu-id="ed0bd-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ed0bd-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ed0bd-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed0bd-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="ed0bd-109">Op: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="ed0bd-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ed0bd-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="ed0bd-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ed0bd-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="ed0bd-111">targets : 'T[]</span></span>

<span data-ttu-id="ed0bd-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="ed0bd-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed0bd-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed0bd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ed0bd-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ed0bd-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed0bd-115">Е</span><span class="sxs-lookup"><span data-stu-id="ed0bd-115">'T</span></span>

<span data-ttu-id="ed0bd-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="ed0bd-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0bd-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="ed0bd-117">See Also</span></span>

- [<span data-ttu-id="ed0bd-118">Microsoft. тактов. Canon. Апплиторест</span><span class="sxs-lookup"><span data-stu-id="ed0bd-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="ed0bd-119">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="ed0bd-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="ed0bd-120">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="ed0bd-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)