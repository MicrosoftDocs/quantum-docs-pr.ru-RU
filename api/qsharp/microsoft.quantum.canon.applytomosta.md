---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Операция Апплитомоста
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: eb793b3d6bc1f75a14e97420d36d0aea3038e0f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850571"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="260bb-102">Операция Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="260bb-102">ApplyToMostA operation</span></span>

<span data-ttu-id="260bb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="260bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="260bb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="260bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="260bb-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="260bb-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="260bb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="260bb-106">Description</span></span>

<span data-ttu-id="260bb-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="260bb-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="260bb-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="260bb-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="260bb-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="260bb-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="260bb-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="260bb-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="260bb-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="260bb-111">targets : 'T[]</span></span>

<span data-ttu-id="260bb-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="260bb-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="260bb-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="260bb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="260bb-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="260bb-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="260bb-115">Е</span><span class="sxs-lookup"><span data-stu-id="260bb-115">'T</span></span>

<span data-ttu-id="260bb-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="260bb-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="260bb-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="260bb-117">See Also</span></span>

- [<span data-ttu-id="260bb-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="260bb-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="260bb-119">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="260bb-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="260bb-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="260bb-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)