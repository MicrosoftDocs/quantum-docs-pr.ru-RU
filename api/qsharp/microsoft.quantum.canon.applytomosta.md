---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Операция Апплитомоста
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 994cada2952809dc84a70b76dc4ede8286c89855
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717204"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="ede9f-102">Операция Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="ede9f-102">ApplyToMostA operation</span></span>

<span data-ttu-id="ede9f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ede9f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ede9f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ede9f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ede9f-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="ede9f-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="ede9f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ede9f-106">Description</span></span>

<span data-ttu-id="ede9f-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ede9f-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ede9f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ede9f-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="ede9f-109">Op: 'T [] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="ede9f-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ede9f-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="ede9f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ede9f-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="ede9f-111">targets : 'T[]</span></span>

<span data-ttu-id="ede9f-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="ede9f-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ede9f-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ede9f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ede9f-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ede9f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ede9f-115">Е</span><span class="sxs-lookup"><span data-stu-id="ede9f-115">'T</span></span>

<span data-ttu-id="ede9f-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="ede9f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ede9f-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="ede9f-117">See Also</span></span>

- [<span data-ttu-id="ede9f-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="ede9f-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="ede9f-119">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="ede9f-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="ede9f-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="ede9f-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)