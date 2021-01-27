---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Операция Апплитотаилк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 8408dff24c5c57efbedb649ac182fac49e836a3e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850419"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="ab193-102">Операция Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="ab193-102">ApplyToTailC operation</span></span>

<span data-ttu-id="ab193-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ab193-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ab193-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab193-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab193-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="ab193-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="ab193-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ab193-106">Description</span></span>

<span data-ttu-id="ab193-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ab193-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ab193-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ab193-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="ab193-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="ab193-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ab193-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="ab193-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ab193-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="ab193-111">targets : 'T[]</span></span>

<span data-ttu-id="ab193-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="ab193-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ab193-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ab193-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ab193-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ab193-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ab193-115">Е</span><span class="sxs-lookup"><span data-stu-id="ab193-115">'T</span></span>

<span data-ttu-id="ab193-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="ab193-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab193-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="ab193-117">See Also</span></span>

- [<span data-ttu-id="ab193-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="ab193-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="ab193-119">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="ab193-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="ab193-120">Microsoft. тактов. Canon. Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="ab193-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)