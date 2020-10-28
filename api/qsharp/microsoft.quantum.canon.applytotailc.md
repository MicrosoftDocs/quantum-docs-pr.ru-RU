---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Операция Апплитотаилк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 631e08666002d8077c6f8b78525b06b104dd4c7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716966"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="f357e-102">Операция Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="f357e-102">ApplyToTailC operation</span></span>

<span data-ttu-id="f357e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f357e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f357e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f357e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f357e-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="f357e-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="f357e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f357e-106">Description</span></span>

<span data-ttu-id="f357e-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f357e-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f357e-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f357e-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="f357e-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="f357e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f357e-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="f357e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f357e-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="f357e-111">targets : 'T[]</span></span>

<span data-ttu-id="f357e-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="f357e-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f357e-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f357e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f357e-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f357e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f357e-115">Е</span><span class="sxs-lookup"><span data-stu-id="f357e-115">'T</span></span>

<span data-ttu-id="f357e-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="f357e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f357e-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="f357e-117">See Also</span></span>

- [<span data-ttu-id="f357e-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="f357e-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="f357e-119">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="f357e-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="f357e-120">Microsoft. тактов. Canon. Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="f357e-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)