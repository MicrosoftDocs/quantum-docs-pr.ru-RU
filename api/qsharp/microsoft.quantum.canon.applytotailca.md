---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Операция Апплитотаилка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 00755df80981a09ddfd8327ee9b35761d30af4f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716938"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="7105b-102">Операция Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="7105b-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="7105b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7105b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7105b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7105b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7105b-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="7105b-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="7105b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7105b-106">Description</span></span>

<span data-ttu-id="7105b-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7105b-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7105b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7105b-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="7105b-109">Op: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="7105b-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7105b-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="7105b-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7105b-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="7105b-111">targets : 'T[]</span></span>

<span data-ttu-id="7105b-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="7105b-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7105b-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7105b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7105b-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7105b-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7105b-115">Е</span><span class="sxs-lookup"><span data-stu-id="7105b-115">'T</span></span>

<span data-ttu-id="7105b-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="7105b-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7105b-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="7105b-117">See Also</span></span>

- [<span data-ttu-id="7105b-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="7105b-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="7105b-119">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="7105b-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="7105b-120">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="7105b-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)